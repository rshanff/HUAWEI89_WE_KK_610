# Makefile generated by Mediatek
# fm support
ifeq ($(MTK_FM_SUPPORT), yes)

#define build_speical_fm_driver

# MT6628 FM driver
#ifeq ($(MTK_FM_CHIP), MT6628_FM)

$(warning feature_option=$(MTK_FM_CHIP))
ifeq ($(findstring MT6628_FM,$(MTK_FM_CHIP)),MT6628_FM)
$(warning MT6628_FM)
	FM_CHIP := mt6628
	FM_CHIP_PATH := $(FM_CHIP)/pub/$(FM_CHIP)
	ccflags-y += -I$(src)/inc \
				-I$(src)/$(FM_CHIP)/inc \
				-I$(src)/../combo/common/include \
				-I$(src)/../combo/common/linux/include \
				-I$(src)/../common_detect
					
obj-$(CONFIG_MTK_FM) += mtk_fm_drv.o
	mt6628-objs	:= core/fm_module.o \
				core/fm_main.o \
				core/fm_config.o \
				core/fm_rds_parser.o \
				core/fm_patch.o \
				core/fm_utils.o \
				core/fm_link.o \
				core/fm_eint.o  \
				$(FM_CHIP_PATH)_fm_lib.o \
				$(FM_CHIP_PATH)_fm_rds.o \
				$(FM_CHIP_PATH)_fm_cmd.o \
				$(FM_CHIP_PATH)_fm_config.o
	mtk_fm_drv-objs += $(mt6628-objs)
$(warning $(mtk_fm_drv-objs))
	#obj-$(CONFIG_MTK_FM) += private/
endif

endif

obj-y += dummy.o

