include ../common.mak

include $(SRCBASE)/.config

all:

install: all
	echo $(CFLAGS)
	install -d $(INSTALLDIR)/usr/sbin
ifeq ($(BUILD_NAME), RT-AC3200)
	install lld2d.rtac3200 $(INSTALLDIR)/usr/sbin/lld2d
	install icon.rtac3200.ico $(INSTALLDIR)/usr/sbin/icon.ico
	install icon.large.rtac3200.ico $(INSTALLDIR)/usr/sbin/icon.large.ico
else ifeq ($(BUILD_NAME), RT-AC56U)
	install lld2d.rtac56u $(INSTALLDIR)/usr/sbin/lld2d
	install icon.rtac56u.ico $(INSTALLDIR)/usr/sbin/icon.ico
	install icon.large.rtac56u.ico $(INSTALLDIR)/usr/sbin/icon.large.ico
else ifeq ($(BUILD_NAME), RT-AC87U)
	install lld2d.rtac87u $(INSTALLDIR)/usr/sbin/lld2d
	install icon.rtac87u.ico $(INSTALLDIR)/usr/sbin/icon.ico
	install icon.large.rtac87u.ico $(INSTALLDIR)/usr/sbin/icon.large.ico
else ifeq ($(BUILD_NAME),$(filter $(BUILD_NAME),RT-AC68U RT-AC68A))
	install lld2d.rtac68u $(INSTALLDIR)/usr/sbin/lld2d
	install lld2d.rtac68p $(INSTALLDIR)/usr/sbin/lld2d.rtac68p
	install lld2d.rtac68r $(INSTALLDIR)/usr/sbin/lld2d.rtac68r
	install lld2d.rtac68w $(INSTALLDIR)/usr/sbin/lld2d.rtac68w
	install lld2d.rtac68rw $(INSTALLDIR)/usr/sbin/lld2d.rtac68rw
	install lld2d.rtac1900 $(INSTALLDIR)/usr/sbin/lld2d.rtac1900
	install lld2d.rtac1900p $(INSTALLDIR)/usr/sbin/lld2d.rtac1900p
	install lld2d.rtac66u_v2 $(INSTALLDIR)/usr/sbin/lld2d.rtac66u_v2
	install lld2d.rtac68a $(INSTALLDIR)/usr/sbin/lld2d.rtac68a
	install lld2d.rtac68uf $(INSTALLDIR)/usr/sbin/lld2d.rtac68uf
	install icon.rtac68u.ico $(INSTALLDIR)/usr/sbin/icon.ico
	install icon.large.rtac68u.ico $(INSTALLDIR)/usr/sbin/icon.large.ico
	install icon.rtac66u_v2.ico $(INSTALLDIR)/usr/sbin/icon_alt.ico
	install icon.large.rtac66u_v2.ico $(INSTALLDIR)/usr/sbin/icon_alt.large.ico
else ifeq ($(BUILD_NAME), RT-AC88U)
	install lld2d.rtac88u $(INSTALLDIR)/usr/sbin/lld2d
	install icon.rtac88u.ico $(INSTALLDIR)/usr/sbin/icon.ico
	install icon.large.rtac88u.ico $(INSTALLDIR)/usr/sbin/icon.large.ico
else ifeq ($(BUILD_NAME), RT-AC3100)
	install lld2d.rtac3100 $(INSTALLDIR)/usr/sbin/lld2d
	install icon.rtac3100.ico $(INSTALLDIR)/usr/sbin/icon.ico
	install icon.large.rtac3100.ico $(INSTALLDIR)/usr/sbin/icon.large.ico
else ifeq ($(BUILD_NAME), RT-AC5300)
	install lld2d.rtac5300 $(INSTALLDIR)/usr/sbin/lld2d
	install icon.rtac5300.ico $(INSTALLDIR)/usr/sbin/icon.ico
	install icon.large.rtac5300.ico $(INSTALLDIR)/usr/sbin/icon.large.ico
else ifeq ($(BUILD_NAME), RT-AC1200G)
	install lld2d.rtac1200g $(INSTALLDIR)/usr/sbin/lld2d
	install icon.rtac1200g.ico $(INSTALLDIR)/usr/sbin/icon.ico
	install icon.large.rtac1200g.ico $(INSTALLDIR)/usr/sbin/icon.large.ico
else ifeq ($(BUILD_NAME), RT-AC1200G+)
	install lld2d.rtac1200g+ $(INSTALLDIR)/usr/sbin/lld2d
	install icon.rtac1200g+.ico $(INSTALLDIR)/usr/sbin/icon.ico
	install icon.large.rtac1200g+.ico $(INSTALLDIR)/usr/sbin/icon.large.ico
else ifeq ($(BUILD_NAME), DSL-AC68U)
	install lld2d.dslac68u $(INSTALLDIR)/usr/sbin/lld2d
	install lld2d.dslac68r $(INSTALLDIR)/usr/sbin/lld2d.dslac68r
	install icon.rtac68u.ico $(INSTALLDIR)/usr/sbin/icon.ico
	install icon.large.rtac68u.ico $(INSTALLDIR)/usr/sbin/icon.large.ico
else
	install lld2d $(INSTALLDIR)/usr/sbin
	install icon.ico $(INSTALLDIR)/usr/sbin
	install icon.large.ico $(INSTALLDIR)/usr/sbin
endif
ifneq ($(RTCONFIG_BCMARM),y)
	install lld2d.conf $(INSTALLDIR)/usr/sbin
else
	cd $(INSTALLDIR)/usr/sbin && ln -sf /tmp/lld2d.conf lld2d.conf
endif

clean:
