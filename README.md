FreeBSD devel/py-pipenv port
============================

Correctly builds and installs with py2 and py3.

- py2: [pr219648][pr219648] needs to be fixed
  - Meantime `pkg install py27-configparser` mitigates the problem
- py3: Locale needs to be set to UTF-8 one

Concurrent install is possible with a patch:

```diff
--- devel/py-virtualenv-clone/Makefile.orig     2017-11-28 03:12:11.508492000 +0000
+++ devel/py-virtualenv-clone/Makefile  2017-11-28 03:12:17.909822000 +0000
@@ -13,6 +13,6 @@

 # Python3 ready
 USES=          python
-USE_PYTHON=    distutils autoplist
+USE_PYTHON=    distutils autoplist concurrent

 .include <bsd.port.mk>
```

[pr219648]: https://bugs.freebsd.org/bugzilla/show_bug.cgi?id=219648
