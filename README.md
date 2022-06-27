# To build

```bash
mkdir tb2-uboot-modern419
cd tb2-uboot-modern419
[[ ! -d modern419 ]] && git clone --branch="modern-4.19" https://github.com/rpardini/u-boot-tb2-asus.git modern419
[[ ! -d rkbin ]] && git clone --branch="linux4.19-rk3399-debian10" https://github.com/TinkerBoard2/rkbin.git
cd rkbin && git reset --hard && git pull --rebase && cd ..
cd modern419 && git reset --hard && git pull --rebase && cd ..
cd modern419 && ./make.sh tinker_board_2 loader --spl --tpl
```

