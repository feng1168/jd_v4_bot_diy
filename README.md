# jd_v4_bot_diy
本仓库只是对Annyoo2021（ https://github.com/Annyoo2021 ）的diy，特此感谢。仅为自用方便，如有侵权请联系我删除，转发请注明出处。

1. jup.sh添加 https://ghproxy.com/ 前缀，对国内网络更友好

# 使用方法
1. 手动执行更新，会自动调用“自定义脚本”(diy.sh)，安装网页控制面板
```
rm -rf /jd/scripts
jup
cd /jd/scripts && npm install png-js && cd ..
```
2. 打开网页控制面板，“自定义脚本”底部添加如下代码并保存，“首页配置”中EnableJupDiyShell的值改为true
```
echo -e "====================== 加载feng1168的diy ======================\n"
wget -q https://ghproxy.com/https://raw.githubusercontent.com/feng1168/jd_v4_bot_diy/main/jup.sh -O /jd/jup_new.sh
if [ -f /jd/jup_new.sh ]; then
  mv -f /jd/jup_new.sh /jd/jup.sh
  chmod +x /jd/jup.sh
  echo -e "加载完成\n"
else
  echo -e "无法下载，请检查网络\n"
fi
```
