
```
cd /usr/src
ncpu=$(sysctl -n hw.ncpu)
sudo make -j$ncpu buildworld
sudo make -j$ncpu buildkernel KERNCONF=CUSTOM
sudo make installkernel KERNCONF=CUSTOM
sudo make installworld
sudo make upgrade
```
