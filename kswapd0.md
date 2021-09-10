## ubuntu14 kswapd0占了太多的CPU


* sudo swapoff /swapfile
* sudo rm  /swapfile
* sudo fallocate -l 8G /swapfile
* sudo chmod 600 /swapfile
* sudo mkswap /swapfile
* sudo swapon /swapfile
