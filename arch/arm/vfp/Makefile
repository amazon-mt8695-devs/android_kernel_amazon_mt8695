#
# linux/arch/arm/vfp/Makefile
#
# Copyright (C) 2001 ARM Limited
#

# ccflags-y := -DDEBUG
# asflags-y := -DDEBUG

vmrs_fpinst    := $(call as-instr,.fpu vfpv2\nvmrs r0$(comma)FPINST,-DHAVE_VMRS_FPINST=1)

KBUILD_CFLAGS  += $(vmrs_fpinst)
KBUILD_AFLAGS  += $(vmrs_fpinst)

LDFLAGS		+=--no-warn-mismatch

obj-y			+= vfp.o

vfp-$(CONFIG_VFP)	+= vfpmodule.o entry.o vfphw.o vfpsingle.o vfpdouble.o
