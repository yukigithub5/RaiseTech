# Swap領域の確保  
* コンピュータが処理を行う際、メモリと呼ばれる場所に処理内容が一時的に記録されます。メモリは容量が決まっており、容量を超えてしまうとエラーで処理が止まってしまいます。Swap領域は、メモリが使い切られそうになった時にメモリの容量を一時的に増やすために準備されるファイル  
## swap領域の用意 *home*～  
* メモリの容量指定し作成  
``` $ sudo dd if=/dev/zero of=/swapfile1 bs=1M count=512 ```  
* 権限変更    
``` $ sudo chmod 600 /swapfile1 ```  
* ファイルをSwapフォーマットに変更  
``` $ sudo mkswap /swapfile1 ```  
* 領域として有効  
``` $ sudo swapon /swapfile1 ```  
# path
``` $ sudo sh -c 'echo "/swapfile1  none        swap    sw              0   0" >> /etc/fstab' ```  
