# For 32-bit system
dtb-$(CONFIG_SEC_MSM895332LTE_CHN) += msm8953-sec-msm8953lte_chn-r00.dtb \
				msm8953-sec-msm8953lte_chn-r01.dtb \
				msm8953-sec-msm8953lte_chn-r02.dtb \
				msm8953-sec-msm8953lte_chn-r03.dtb 

# For 64-bit system
dtb-$(CONFIG_SEC_MSM8953LTE_CHN) += msm8953-sec-msm8953lte_chn-r00.dtb \
				msm8953-sec-msm8953lte_chn-r01.dtb \
				msm8953-sec-msm8953lte_chn-r02.dtb \
				msm8953-sec-msm8953lte_chn-r03.dtb

# For C7LTE_CHN
dtb-$(CONFIG_SEC_C7LTE_CHN) += msm8953-sec-c7lte_chn-r00.dtb \
				msm8953-sec-c7lte_chn-r01.dtb \
				msm8953-sec-c7lte_chn-r02.dtb \
				msm8953-sec-c7lte_chn-r03.dtb \
				msm8953-sec-c7lte_chn-r04.dtb

# For C7LTE_KOR_SKT
dtb-$(CONFIG_SEC_C7LTE_KOR_SKT) += msm8953-sec-c7lte_kor_skt-r00.dtb

# For ON7XLTE_CHN
dtb-$(CONFIG_SEC_ON7XLTE_CHN) += msm8953-sec-on7xlte_chn-r00.dtb

# For GTAXLQLTE_USA_SPR
dtb-$(CONFIG_SEC_GTAXLQLTE_USA_SPR) += msm8953-sec-gtaxlqlte_usa_spr-r00.dtb

ifeq ($(CONFIG_ARM64),y)
always          := $(dtb-y)
subdir-y        := $(dts-dirs)
else
targets += dtbs
targets += $(addprefix ../, $(dtb-y))

$(obj)/../../%.dtb: $(src)/%.dts FORCE
        $(call if_changed_dep,dtc)

dtbs: $(addprefix $(obj)/../../,$(dtb-y))
endif
clean-files := *.dtb *.reserve.dts
