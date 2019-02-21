# docker-openwrt-buildroot

#image for building openwrt

git clone https://github.com/openwrt/chaos_calmer.git

docker run -it --name="openwrt" -v ${PWD}/chaos_calmer:/home/openwrt/chaos_calmer serh/docker-openwrt-buildroot

cd /home/openwrt/chaos_calmer

./scripts/feeds update -a

make menuconfig

make V=sc
