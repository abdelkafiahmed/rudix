# Author: Qichang Liang <kcleung@cs.otago.ac.nz>

BuildRequires += $(LibDir)/libgmp.la  # static-gmp
BuildRequires += $(LibDir)/libmpfr.la  # static-mpfr

include ../../Library/GNU.mk

Description=	C library for arbitrary precision arithmetic on complex numbers 
Summary=	The GNU MPC library
Title=		GNU MPC
Name=		mpc
Version=	1.0.3
Site=		http://www.multiprecision.org/
Source=		ftp://ftp.gnu.org/gnu/mpc//$(Name)-$(Version).tar.gz
License=	LGPLv3
LicenseFile=	$(SourceDir)/COPYING.LESSER

GnuConfigureExtra += --with-pic

ifeq ($(OSXVersion),10.6)
RUDIX_UNIVERSAL=no
endif

define test_hook
test -f $(LibDir)/libmpc.la
endef
