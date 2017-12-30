# $FreeBSD$

PORTNAME=	pipenv
PORTVERSION=	9.0.1
CATEGORIES=	devel python
MASTER_SITES=	CHEESESHOP
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	snsinfu@gmail.com
COMMENT=	Dependency manager for Python projects

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/LICENSE

RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}virtualenv>0:devel/py-virtualenv@${FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}pew>=0.1.26:devel/py-pew@${FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}pip>=9.0.1:devel/py-pip@${FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}requests>=2.18.1:www/py-requests@${FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}flake8>=3.0.0:devel/py-flake8@${FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}urllib3>=1.21.1:net/py-urllib3@${FLAVOR}

USES=		python
USE_PYTHON=	distutils autoplist concurrent

NO_ARCH=	yes

.include <bsd.port.mk>
