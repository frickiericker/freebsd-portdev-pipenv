FreeBSD devel/py-pipenv port
============================

Correctly builds and installs with py2 and py3.

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
