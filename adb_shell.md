
adb ��β鿴����cpu���ڴ�ռ����
1. adb shell
2. top | grep PID
top -m 20 -t �鿴ĳ���߳�ռ��cpu��Դ

toolbox top -t -s cpu -m 20

###############################################################################
A50���ĺ�
echo 1800000 4 0 0 1800000 4 0 0 > /sys/devices/platform/soc/cpu_budget_cooling/roomage
chmod 440 /sys/devices/platform/soc/cpu_budget_cooling/roomage

���һ�� roomage�ڵ��ǲ��� 1800000 4 0 0 1800000 4 0 0�� �������� �������Ƶ �ĺ�ȫ��
####################################################################################

 �鿴���������ĸ�cpu��
 ps -A -o NAME -o CPU | grep media
#######################################################################

�鿴�жϺ�
cat  /proc/inter*

���жϰ󶨵���������
�����жϺ�Ϊ197 
/proc/irq/197 # cat smp_affinity_list

echo 2 > smp_affinity_list
########################################################################

ץ����tcpdump -i wlan0 -s 0 -w /sdcard/rtmp.pcap -v

��������busybox ifconfig

�鿴ϵͳʱ����Դ��
  /sys/kernel/debug/clk/clk_sum

u�̶�/д���ʵĲ�������ֱ����£�
1������д���ʣ�
time dd if=/dev/zero of=/mnt/usb/test.bin bs=500000 count=1000
2�����Զ����ʣ�
time dd if=/mnt/usb/test.bin bs=500000 count=1000 of=/dev/null

����cma�ڴ�
sunxi#env set cma 650M
sunxi#env save
Saving Environment to SUNXI...
saveenv storage_type = 2
sunxi#env print cma
cma=600M

androidO ��ʾ֡��
 setprop debug.hwc  on.fps  ��ʾ֡�ʣ�
  setprop debug.hwc  on.show  ÿһ֡��layer��Ϣ�����ӡ����


adb logcat
ȥ��ĳ���ļ���Ĵ�ӡ adb logcat IMGSRV:s  (IMGSRV�ļ�)


adb ����apk
adb shell am start -n [package name]/[apkMainActivity]
��AndroidManifest.xml��package="com.example.helloworld"�õ�package name
<activity
            android:name=".MainActivity"
            android:label="@string/app_name" >
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />

                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
		activity���Եõ�MainActivity
�磺 am start -n com.example.helloworld/com.example.helloworld.MainActivity

����tvdLauncher
am start -n com.softwinner.launcher/com.softwinner.launcher.Launcher

������Ϊ��Ƶͨ����pk
am start -n com.huawei.iptv.stb.videotalk.activity/.MainActivity

H3����ͼ��apk
am start -n com.android.gallery3d/com.android.gallery3d.app.GalleryActivity
com.android.gallery3d.app.GalleryActivity

�������
am start -n com.android.camera2/com.android.camera.CameraActivity

����������
am start -n com.softwinner.TvdVideo/com.softwinner.TvdVideo.TvdVideoActivity -d https://fs-sq-1.kfs.io/201307/2d8qY-MrgmhzkHYXl7UFKIgDA33jUomeZ1o9vMsUN8I=?play_mode=openapi&__gda__=1468392340_1dde9aad4adf195519096edbbcc60bfc

"http://pl.youku.com/playlist/m3u8?ts=1456996755&keyframe=1&vid=XMTQzMDE1NTMwOA==&type=hd2&ctype=20&sid=345699675553920d0a321&token=9056&ev=1&oip=1900834927&did=eabca10cf602692b8e64b59d908e6c0deabca10c&ep=9Jk5MdwNbw3S9D0W4mdWvPo8Nk2qa0cfqmdMtQyb%2FiRx94SJlur%2Ff0u15eVSknm%2B%0A"

http://60.19.28.11:18011/4k/8.mp4

http://192.168.152.7:8080/h265.ts

����apk
am start -n com.hisense.mediacenter.mediaplayer/com.hisense.mediacenter.LaunchActivity

�Ĵ�����Ϸ
�˺ţ� 112.4.29.129


����IPTV
��ţƽ̨
SN��
00000100000760600001AC4AFE2BAAA0 �����˺���ɾ����
MAC��
AC4AFE2BAAA0 
�û�����
HSTEST00004@IPTV
���룺
340998

SN&MAC����?
00000100000760600001AC4AFE2BAAA6
HS0471000098@IPTV
030014

��������IPTV�����м��
��¼������Ҫ��uboot���ô��ڣ���s������������uboot��
Ȼ��setenv console ttyS0,115200��Ȼ��saveenv��Ȼ��reset����
�����պ��Ǻ���״̬����Ҫ��ң�ص����ü��������ã�����6321��
Ȼ����߼�����ȥѡ��Ϊƽ̨�������˺�haixin4������haixin4���㱣�档
���Ӧ�û�Ҫȥ����������ѡ���Զ���ȡip��Ȼ�������Ϳ��Խ�ȥ��
������֤��ַ�� 
http://60.31.30.231:33200/EPG/jsp/AuthenticationURL 
http://60.31.30.231:33200/EPG/jsp/AuthenticationURL

fastboot��ִ��������дMAC&&SN
pst erase 
save_userdata mac  AC:4A:FE:2B:AA:A0 

save_userdata specialstr 00000100000760600001AC4AFE2BAAA6 

��Ϊƽ̨��
haixin3
haixin3

��������
MAC��48:55:5F:FF:B8:06
 �˺ţ�980192278849
  ���룺38384255

4.10�Ź̼�
��Ҫ�˺����룺
MAC: AC4AFE9FB159
�û�����hs0407test2
��  �룺123456



hw/audio_policy.default.so
(17:28) �ƻݱ�: �ƿ����
(17:29) �ƻݱ�: ����Ҫ busybox killall mediaserver

 �鿴VEƵ��
root@rabbit-p1:/sys/class/sunxi_dump # echo 0x01c20018 > dump                  
root@rabbit-p1:/sys/class/sunxi_dump # cat dump    
0x91000e00
24*N/M������N a=(14:8 bit), b=(3:0 bit), N=a+1, M=b+1; �� 0x91000e00�� ��Ϊ 360M





���ڲ�����
115200

android7.0 drm��Ƶ����
�˺� liling19930619@gmail.com
���� ling1993

leegreatworld
egreatworld


hls��̬����ƬԴ
http://www.youtube.com/api/manifest/hls_variant/id/0168724d02bd9945/itag/5/source/youtube/playlist_type/DVR/ip/0.0.0.0/ipbits/0/expire/19000000000/sparams/ip,ipbits,expire,id,itag,source,playlist_type/signature/773AB8ACC68A96E5AA481996AD6A1BBCB70DCB87.95733B544ACC5F01A1223A837D2CF04DF85A3360/key/ik0/file/m3u8

�ر�selinux




echo 4 > /sys/kernel/autohotplug/lock
echo 0-3 > /dev/cpuset/foreground/cpus

���ˣ�  /sys/kernel/autohotplug/enable   // 1 Ĭ�ϴ�
        ��echo 4 > /sys/kernel/autohotplug/lock  //��4��

��Ƶ��  echo 1200000 > /sys/devices/system/cpu/cpu0/cpufreq/scaling_max_freq
        ��echo 1200000 > /sys/devices/system/cpu/cpu0/cpufreq/scaling_min_freq   //4��������1.2G 

������cat /sys/devices/system/cpu/cpu0/cpufreq/scaling_cur_freq  //�鿴0��cpu��ǰƵ��


�ڴ����
lsof | grep dmabuf|grep mem

cts ���Ե�����Է���

��activity 
ֱ��am am start -n ����/activity ·��������

û��activity

am instrument -r -e class android.media.cts.AdaptivePlaybackTest#testHEVC_adaptiveDrc -w android.media.cts/android.support.test.runner.AndroidJUnitRunner

����˵��
android.media.cts.AdaptivePlaybackTest#testHEVC_adaptiveDrcs �ǰ��������ӷ�������
android.media.cts  ����
android.support.test.runner.AndroidJUnitRunner AndroidManifest ���� instrument ���ѡ��



�ο�
http://www.bkjia.com/Androidjc/1009016.html
