# $FreeBSD$

PORTNAME=	pew
PORTVERSION=	1.1.1
CATEGORIES=	devel python
MASTER_SITES=	CHEESESHOP
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	snsinfu@gmail.com
COMMENT=	Tool to manage multiple virtualenvs written in pure python

LICENSE=	MIT

RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}virtualenv>=1.11:devel/py-virtualenv \
		${PYTHON_PKGNAMEPREFIX}virtualenv-clone>=0.2.5:devel/py-virtualenv-clone

USES=		python shebangfix
USE_PYTHON=	distutils autoplist concurrent

NO_ARCH=	yes
SHEBANG_FILES=	pew/shell_config/complete_deploy

.include <bsd.port.pre.mk>

.if ${PYTHON_REL} < 3000
RUN_DEPENDS+=	${PYTHON_PKGNAMEPREFIX}backports.shutil_get_terminal_size>=0:devel/py-backports.shutil_get_terminal_size \
		${PYTHON_PKGNAMEPREFIX}shutilwhich>=0:sysutils/py-shutilwhich
.endif
.if ${PYTHON_REL} < 3400
RUN_DEPENDS+=	${PYTHON_PKGNAMEPREFIX}pathlib>=0:devel/py-pathlib
.endif

.include <bsd.port.post.mk>
