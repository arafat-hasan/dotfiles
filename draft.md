ফিস শেলের সাথে ইন্টেল আইজে চালাতে `XDG_CONFIG_HOME` সেট করতে হয়। তাছাড়া ইন্টেল আইজের প্রজেক্ট রুটে '$HOME' নামে ডিরেক্টরি তৈরি হয়।
```
set -U XDG_CONFIG_HOME "$HOME/.config"
```


## BBC বাংলায় ফন্ট সমস্যা
উবুন্তুর ফায়ারফক্সে বিবিসি বাংলা ফন্ট ভেঙে যাওয়ার সমস্যা ছিল। খুজে দেখা গেল যে FreeSans ফন্ট ব্যবহৃত হচ্ছে যা সিস্টেমে ইন্সটল নেই। অতপর ইন্সটল করা হলো। এছাড়ায় নোটো বেঙ্গলি ফ্যামিলি ও অন্যান্য বাংলা ফন্ট ইন্সটল করা হলো। fonts ডিরেক্টরিতে সকল ফন্ট আছে।

```
sudo cp -a . /usr/local/share/fonts/
```



## Start Slack Minimized on Startup

Gnome startup application এ স্লাক সংযুক্ত করে কমান্ড দিতে হবে `slack -u %U`। অথবা নিচের ঠিকানায় নিচের টেক্সট রাখতে হবে।

~/.config/autostart/slack.desktop
```
[Desktop Entry]
Type=Application
Exec=slack -u %U
Hidden=false
NoDisplay=false
X-GNOME-Autostart-enabled=true
Name[en_US]=Slack
Name=Slack
Comment[en_US]=Slack Desktop
Comment=Slack Desktop
```
