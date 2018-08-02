
# mac 优化性能 tips 
 
 # 关闭Spotlight

 
有时候 macOS 的 Spotlight 索引会占用太多系统资源，特别是在频繁更新、添加、删除大量文件的时候，这种情况下，有两个办法，一个是使用系统偏好设置，将整个磁盘或者对应文件夹添加到不检查列表中。另外一个是关闭索引功能…

## 关闭索引
/# turn off for all volumes:
sudo mdutil -a -i off
/# turn off for specific volumes:
sudo mdutil -i off "/Volumes/Machintosh\ HD"
/# turn on for all volumes:
sudo mdutil -a -i on


## unload metadata:
/# unload
sudo launchctl unload -w /System/Library/LaunchDaemons/com.apple.metadata.mds.plist
/# load
sudo launchctl load -w /System/Library/LaunchDaemons/com.apple.metadata.mds.plist




