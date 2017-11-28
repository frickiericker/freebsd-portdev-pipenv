FreeBSD devel/py-pipenv port
============================

Correctly builds and installs with py2 and py3.

- py2: [pr219648][pr219648] needs to be fixed
  - Meantime `pkg install py27-configparser` mitigates the problem
- py3: Locale needs to be set to UTF-8 one

[pr219648]: https://bugs.freebsd.org/bugzilla/show_bug.cgi?id=219648
