# $FreeBSD$

PROG=	fdisk
SRCS=	fdisk.c geom_pc98_enc.c
WARNS?=	4
MAN=	fdisk.8

.PATH:	${.CURDIR}/../../sys/geom

LIBADD=	geom

.include <bsd.prog.mk>
