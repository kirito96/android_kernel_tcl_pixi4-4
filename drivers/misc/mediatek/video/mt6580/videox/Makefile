# drivers/video/mtk/Makefile
#

obj-$(CONFIG_MTK_FB) += mtkfb_console.o        \
						disp_assert_layer.o    \
						debug.o                \
						primary_display.o      \
						disp_lcm.o             \
						disp_utils.o           \
						mtk_disp_mgr.o         \
						mtk_mira.o             \
						mtk_ovl.o              \
						disp_dts_gpio.o        \
						disp_helper.o

ccflags-y += -I$(srctree)/drivers/misc/mediatek/video/include/     \
             -I$(srctree)/drivers/misc/mediatek/video/common/      \
             -I$(srctree)/drivers/misc/mediatek/video/common/rdma10/ \
             -I$(srctree)/drivers/misc/mediatek/video/common/wdma10/ \
             -I$(srctree)/drivers/misc/mediatek/video/$(MTK_PLATFORM)/dispsys   \
             -I$(srctree)/drivers/misc/mediatek/sync/      \
             -I$(srctree)/drivers/misc/mediatek/m4u/$(MTK_PLATFORM)       \
             -I$(srctree)/drivers/misc/mediatek/cmdq/v2/ \
             -I$(srctree)/drivers/misc/mediatek/cmdq/v2/$(MTK_PLATFORM)/ \
             -I$(srctree)/drivers/misc/mediatek/externaldisplay/$(MTK_PLATFORM) \
             -I$(srctree)/drivers/misc/mediatek/mach/$(MTK_PLATFORM)/include/mach/ \
             -I$(srctree)/drivers/staging/android/ion/ \
             -I$(srctree)/drivers/misc/mediatek/base/power/$(MTK_PLATFORM) \
             -I$(srctree)/drivers/misc/mediatek/base/power/include/spm_v1/ \
             -I$(srctree)/drivers/misc/mediatek/base/power/include/ \
             -I$(srctree)/drivers/misc/mediatek/m4u/$(MTK_PLATFORM)/ \
             -I$(srctree)/drivers/misc/mediatek/mmp/
ccflags-y += -I$(srctree)/drivers/staging/android/ion/
ccflags-$(CONFIG_MTK_LCM) += -I$(srctree)/drivers/misc/mediatek/lcm/inc/
ccflags-y += -I$(srctree)/drivers/staging/android/ion \
             -I$(srctree)/drivers/staging/android/ion/mtk

ifeq ($(CONFIG_MTK_INTERNAL_HDMI_SUPPORT), y)
ccflags-y += -I$(srctree)/drivers/misc/mediatek/hdmi/
endif
ifeq ($(CONFIG_MTK_INTERNAL_MHL_SUPPORT), y)
ccflags-y += -I$(srctree)/drivers/misc/mediatek/mhltx/
endif
ifeq ($(CONFIG_MTK_DITHERING_SUPPORT), y)
ccflags-y += -DDITHERING_SUPPORT
endif

ifeq ($(CONFIG_MTK_GPU_SUPPORT), y)
ccflags-y += -DHWGPU_SUPPORT
endif
