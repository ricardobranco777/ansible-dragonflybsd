
```
cd /usr/src
sudo make buildworld
make buildkernel KERNCONF=CUSTOM
sudo make installkernel KERNCONF=CUSTOM
sudo make installworld
sudo make upgrade
```
