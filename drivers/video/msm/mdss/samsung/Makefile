#
#	PLEASE ADD BELOW LINE at /android/kernel/driver/makefile
#
#	ifeq ($(CONFIG_FB_MSM_MDSS_SAMSUNG),y)
#	LINUXINCLUDE	+=  -I$(srctree)/drivers/video/msm/mdss/samsung/
#	endif


#
# Samsung Common file.
#
obj-y += ss_dsi_panel_common.o
obj-y += ss_dsi_mdnie_lite_common.o
obj-y += ss_dsi_smart_dimming_common.o
obj-$(CONFIG_SAMSUNG_DEBUG_DISPLAY) += dlog.o
#
# panel directory make file
#

# TO SUPPORT PBA BOOINT
obj-y += PBA_BOOTING_HD/

# MSM8953
# C7 panel
obj-$(CONFIG_PANEL_S6E3FA3_AMS568HN31_FHD) += S6E3FA3_AMS568HN31/

# A9 panel
obj-$(CONFIG_PANEL_S6E3FA3_AMS598KH01_FHD) += S6E3FA3_AMS598KH01/

#Elite
obj-$(CONFIG_PANEL_SC7798D_BV038WVM_WVGA) += SC7798D_BV038WVM/

# IN_CELL panel
obj-$(CONFIG_PANEL_HX83100A_C5001H3F_HD) += HX83100A_C5001H3F/

# IN_CELL panel
obj-$(CONFIG_PANEL_TD4100_C5001H3F_HD) += TD4100_C5001H3F/

# On7X IN_CELL panel
obj-$(CONFIG_PANEL_TD4300_BS055FHM_FHD) += TD4300_BS055FHM/

