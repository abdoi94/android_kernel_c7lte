ifeq ($(CONFIG_OF),y)

ifeq ($(CONFIG_SEC_ON5QLTE_PROJECT),y)
        ifeq ($(CONFIG_MACH_ON5QLTE_CHN_OPEN),y)
                dtb-y += msm8917-sec-on5qlte-chn-r00.dtb
		dtb-y += msm8917-sec-on5qlte-chn-r01.dtb
        endif
endif

ifeq ($(CONFIG_SEC_ELITELTE_PROJECT),y)
        ifeq ($(CONFIG_MACH_ELITELTE_CHN_OPEN),y)
                dtb-y += msm8917-sec-elitelte-chn-r00.dtb
		dtb-y += msm8917-sec-elitelte-chn-r01.dtb
		dtb-y += msm8917-sec-elitelte-chn-r02.dtb
        endif
endif

echo '*** Warning: Samsung $@ Device Tree MSM8917.'
DTB_NAMES := $(subst $\",,$(CONFIG_BUILD_ARM_APPENDED_DTB_IMAGE_NAMES))
ifneq ($(DTB_NAMES),)
DTB_LIST := $(addsuffix .dtb,$(DTB_NAMES))
else
DTB_LIST := $(dtb-y)
endif

targets += dtbs
targets += $(addprefix ../, $(DTB_LIST))
endif

$(obj)/../../%.dtb: $(src)/%.dts FORCE
	$(call if_changed_dep,dtc)

dtbs: $(addprefix $(obj)/../../,$(DTB_LIST))

clean-files := *.dtb *.reverse.dts


