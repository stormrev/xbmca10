include ../depends.mk

CONFIGURE=./configure \
	--prefix=$(PREFIX) \
	--build=$(BUILD) \
	--host=$(HOST) \
	--disable-x11 \
	--disable-sdl \
	--disable-xrandr \
	--disable-joystick \
	--disable-gl \
	--disable-vdpau \
	--disable-vaapi \
	--disable-openmax \
	--enable-neon \
	--enable-gles \

SRC=../../../../

all: dep
	(cd $(SRC); make)

bin-only:
	(cd $(SRC); make)

dep: bootstrap configure

bootstrap:
	(cd $(SRC); ./bootstrap)

configure:
	(cd $(SRC); $(CONFIGURE))