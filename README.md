# To build

```bash
mkdir tb2-uboot-modern
cd tb2-uboot-modern
[[ ! -d u-boot-tb2-asus ]] && git clone --branch="modern" https://github.com/rpardini/u-boot-tb2-asus.git
[[ ! -d rkbin ]] && git clone --branch="linux4.19-rk3399-debian10" https://github.com/TinkerBoard2/rkbin.git
cd rkbin && git reset --hard && git pull --rebase && cd ..
cd u-boot-tb2-asus && git reset --hard && git pull --rebase && cd ..
cd u-boot-tb2-asus && ./make.sh tinker2 --spl --tpl
```

