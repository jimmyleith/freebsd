# $FreeBSD$

PROG=	kdigest
MAN=	kdigest.8
CFLAGS+=	-I${KRB5DIR}/lib/asn1 \
		-I${KRB5DIR}/lib/roken \
		-I${KRB5DIR}/lib/sl -I.
LIBADD=	krb5 heimntlm roken crypto edit sl vers
SRCS=	kdigest.c \
	kdigest-commands.c \
	kdigest-commands.h

kdigest-commands.h: kdigest-commands.in
	${SLC} ${.ALLSRC:M*.in}

.for ext in c o
kdigest-commands.${ext}: kdigest-commands.h
.endfor

.include <bsd.prog.mk>

.PATH: ${KRB5DIR}/kuser
