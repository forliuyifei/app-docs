---
title: VIPER4Android FX
description: 拯救你糊成一坨的音效
type: docs
date: 2020-12-24 23:09:51
update: 2020-12-24 23:09:51
---

[xda 发布页](https://www.xda-developers.com/viper4android-v2-7-new-ui-profile-management/)

## 蝰蛇音效驱动
~~旧安装方法失效~~
下面的方法适用于 Android 11
1. 使用 Magisk 刷入 [Selinux_Permissiver_Magisk.zip](https://lanzoui.com/iW75cj1wqkd) ，**重启生效**
   如果您十分看重自己手机的安全性，建议保持 SELinux 的正常启用，放弃使用兼容模式。
2. 在 Magisk 仓库下载并安装 ViPER4Android FX （我这里的版本是 2.7.2.1）
3. 重启后打开 ViPER4Android FX 应用，仍然显示驱动未安装，给它 root 权限，确认安装，加载过程中应该会出现 “Magisk” 字样。（*运气不好的同学慎用这种安装驱动的方式，可能导致无法开机且不容易解决*）
4. 重启手机，打开 ViPER4Android FX，点击右上角中间的图标查看驱动程序状态：
   - 显示 NEON 已启用：否
   - 驱动状态：不正常
   - 音频格式：不支持
 5. 进设置 **启用 Legacy mode 开关**。回到软件主界面，查看驱动状态，一切正常 🙏
 6. 随便放首歌试试效果 d🙉b
   相关配置文件存放目录：`Android/data/com.pittvandewitt.viperfx/files`
   分享一个旧版的配置包：[ViPER4Android.zip](https://lanzoui.com/iCIVij202mf)，Kernel 目录下的文件还能用，HIFI.irs 的效果最好，在 **脉冲反馈样本** 列表中选用它，Enjoy。
   XDA 上有大佬发布了新旧配置文件的转换工具，感兴趣的可以看看。（我这里转换成功但依然无法使用）
7. PS：此版本的软件界面经过简化，不再同时显示多音频设备的配置栏目，比如有线耳机相关的配置开关仅在插入耳机时展示。

## 配置项说明
![2.7.2.1截图](https://cdn.jsdelivr.net/gh/forliuyifei/img@mater/img/2020/12/1608062970609.webp)
不懂声学，机翻 + 少量润色，请多多包涵，欢迎指出改进意见。

### 回放增益控制
Mainly used to dynamically control, amplify or attenuate the audio volume.
主要用于动态控制，放大或衰减音频音量。

**Gain Ratio 效果级别**
Gain Ratio is the speed of amplification or attenuation, the stronger, the faster the speed and the higher the final volume. The weaker, the slower the speed, the closer to the original volume.
增益比是放大或衰减的速度，越强，速度越快，最终音量越高。 越弱，速度越慢，越接近原始音量。

**Max Gain 最大增益倍数**
When the volume is too low, use this parameter to uplevel the sound, there may be very large magnification. The higher the value, the louder the volume. But too large will also amplify the noise within the song.
当音量太低时，使用此参数将声音放大，可能会有很大的放大倍数。 值越高，音量越大。 但是太大会放大歌曲中的噪音。

**Max Output 最大音量**
This value defines the maximum volume of the Playback AGC sound in dB, the greater the value the greater the volume; 0 dB is the maximum.
该值定义了回放AGC声音的最大音量（以dB为单位），值越大音量越大； 最大为0 dB。

### 场效应压缩器
The field-effect transistor (FET) is a type of transistor which uses an electric field to control the flow of current. FETs are devices with three terminals: source, gate, and drain. FETs control the flow of current by the application of a voltage to the gate, which in turn alters the conductivity between the drain and source.
ViPER is capable of simulating this system.
场效应晶体管（FET）是一种使用电场控制电流流动的晶体管。  FET是具有三个端子的设备：源极，栅极和漏极。  FET通过向栅极施加电压来控制电流，从而改变漏极和源极之间的电导率。
ViPER能够模拟此系统。

**Threshold 工作门限**
The threshold control sets the level at which the compression effect is engaged. Only when a level passes above the threshold will it be compressed. If the threshold level is set at say -10 dB, only signal peaks that extend above that level will be compressed. The rest of the time, no compression will be taking place.
阈值控件设置了压缩效果所处的级别。 只有当级别超过阈值时，它才会被压缩。 如果将阈值级别设置为-10 dB，则仅压缩超出该级别的信号峰值。 其余时间，将不会进行压缩。

**Ratio 压缩比率**
Compression ratio specifies the amount of attenuation to be applied to the signal.
压缩比指定要应用于信号的衰减量。

**Knee 拐点**
The “knee” refers to how the compressor transitions between the non-compressed and compressed states of an audio signal running through it.
“拐点”是指压缩器如何在通过它的音频信号的非压缩状态和压缩状态之间转换。

**Attack 起音**
This refers to the time it takes for the signal to become fully compressed after exceeding the threshold level.
这是指信号在超过阈值水平后变为完全压缩所花费的时间。

**Release 释音**
This is literally the opposite of attack time. More specifically, it is the time it takes for the signal to go from the compressed — or attenuated — state back to the original non-compressed signal. Release times will be considerably longer than attack times.
这实际上与起音时间相反。 具体而言，它是信号从压缩（或衰减）状态返回到原始非压缩信号所花费的时间。 释音时间将比起音时间长得多。

**Gain 增益**
Raise the volume of the result

**Crest 波峰**
Distance between the highest and electrically average audio
最高频和平均声音频率之间的差值

**Adapt 适应**
Time to average
适应（所需？）时间

**Clipping prevention 组织削波**
To prevent static-like artifacts when the volume is too high to work with
当音量过高以至于无法使用时，防止产生类似静电的 artifacts（不会翻译）

### VIPER-DDC
This feature allows users to load VDC headset correction files. These files are headphone-specific and are normally used to neutralize the frequency response. This means that the lows, mids and highs are not emphasized over another, which is similar to reference grade headphones. DDCs are based on Parametric EQ filters and can also be used for non-correction purposes.
此功能允许用户加载VDC耳机校正文件。 这些文件是专机专用的，通常用于抵消频率响应。 这意味着低、中、高频不会互相覆盖（*大概是这个意思*），类似于参考级耳机。  DDC基于参数均衡器滤波器，也可用于非校正目的。

### 频谱拓展
Makes your music sound lossless with enhanced high frequencies.
It calculates what of the frequency spectrum is lost and is useful if you play lossy audio files
If turned on, the audio spectrum will be reconstructed to recover high frequencies (16k~22kHz), just like Sony DSEE.
拓展高频，使您的音乐“无损”。
它可以计算丢失了哪些频谱，如果您播放有损音频文件，该功能将非常有用
如果打开，音频频谱将被重建以恢复高频（16k〜22kHz），就像Sony DSEE一样。

### FIR 均衡器
511-order 10 bands FIR linear equalizer
Adjust the levels of amplification and attenuation of all 10 bands
511阶、10频段的 FIR 线性均衡器
调整所有10个频段的放大和衰减水平

### 脉冲反馈处理
Once an impulse response has been loaded, music will show the same characteristics as the loaded sample.
加载脉冲响应后，音乐将显示与加载样本相同的特征。

**Crosschannel 通道交叉比例**
Upmixes stereo to quad-channel, like this:
Channel 1: Left channel
Channel 2: x% of right channel
Channel 3: x% of left channel
Channel 4: Right channel
(x = crosschannel value)
将立体声上混到四声道，如下所示：
声道1：左声道
声道2：右声道的x％
声道3：左声道的x％
声道4：右声道
 （x = 通道交叉比例）
 
This parameter has no effect when using quad-channel impulse responses
使用四通道脉冲响应时，此参数无效

### 场环绕
Create sound field surround effects.
The sound field can be understood as a mono or stereo field
创建声场环绕效果。
声场可以理解为单声道或立体声场

**Surround strength 场环绕强度**
Defines the strength of the field surround effects. The stronger, the stereo effect will be more obvious, the sound will come from left and right sides.
定义场环绕效果的强度。 声音越强，立体声效果将越明显，声音将来自左右两侧。

**Mid image strength 中心强度**
Defines the central vocal intensity. More strong man sounds more clear, the weaker the more ethereal sound.
定义中央人声强度。 越强则人声越清晰，越弱则声音越空灵。

### 差分环绕
Also known as the precedence or haas effect.
The law discoved in 1949 states that when one sound is followed by another with a delay time of approximately 40 ms or less (below humans’ echo threshold), the two are perceived as a single sound.
This relates to how we determine spatial location by sound. Because two noises with a very short delay between them are perceived as one, spatial location is determined by the first heard, dominant sound–regardless of where the second came.
也称为优先或哈斯效应。
一条发现于1949年的规律表明，当一种声音紧随另一种声音的延迟时间约为40毫秒或更短（低于人类的回声阈值）时，这两种声音将被当作一种声音。
这与我们如何通过声音确定空间位置有关。 由于两个噪声之间的延迟很短，因此它们被视为一个噪声，因此空间位置取决于听到的第一个主导声音，而不管第二个噪声来自何处。

Delay 延时
Defines the delay between left and right. The greater, the wider the sound.
定义左右声道之间的延迟。 延时越大，声音越 “宽” 。

### 耳机环绕+
Virtual Headphone Surround effect
虚拟耳机环绕效果

Level 效果强度
Strength of VHS+

### 数字混响
Reverberation uses mathematical methods to simulate an environmental feeling. For example, a song can be felt playing inside the auditorium, living room, bathroom, and so on.
混响就是使用数字技术模拟 “环境感” 。 例如，播放一首歌时可以让人感觉自己在礼堂，客厅，浴室等场所内部。

**Room size 房间大小**
Defines the virtual environment area size. The larger the value, the wider the sound
定义虚拟环境区域的大小。 值越大，声音越宽。

**Sound field 声场大小**
Defines the width of the room above, in meters. Assumed that the above room size is 100 square meters, here to set a width of 14 meters, then the length of the room will be 7.14 m.
Therefore, the room size and width defines the aspect ratio of the virtual environment. The larger the value, the sound coming from both sides will felt more obvious.
定义上方房间的宽度（以米为单位）。 假设上述房间大小为100平方米，此处将宽度设置为14米，则房间的长度将为7.14 m。
因此，房间的大小和宽度定义了虚拟环境的纵横比。 值越大，从两侧传来的声音会越明显。

**Damping factor 水汽含量**
Defines the humidity of air in the above virtual environment, the moisture vapor in the air will easily absorb the echoes. The bigger this value, the less echoes heard.
在上述虚拟环境中定义空气的湿度，回声很容易被空气中的水汽吸收。 该值越大，回声就越少。

**Dry signal 原始信号比例**
Defines the volume of the original sound
定义原始声音的音量

**Wet signal 混响信号比例**
Defines the volume of the simulated environment effect
定义模拟环境效果的音量

For environments with low air humidity such as living rooms, auditoriums and other indoor environments, you can use room size and sound field to define the area of ​​the virtual environment: water vapor content values ​​from 0 to 20, the reverb signal values ​​20 to 50, the proportion of the original signal to take value of about 50. For environments with high air humidity such as bathrooms and other indoor environments that contain a lot of moisture, you can use room size and sound field to define the area of ​​the virtual environment: water vapor content values ​​of 50 to 100, the reverb signal values ​​40 to 80, the proportion of the original signal value of about 50.
对于客厅，礼堂等室内空气湿度较低的环境，您可以使用房间大小和声场来定义虚拟环境的区域：水蒸气含量值从0到20，混响信号 值介于20到50之间，原始信号所占的比例约为50.对于空气湿度高的环境，例如浴室和其他含水量很大的室内环境，可以使用房间大小和声场来定义 虚拟环境区域：水蒸气含量值在50到100之间，混响信号值在40到80之间，原始信号值的比例约为50。

### 动态系统
Handles the dynamic range of the sound. In other words the bass, treble, and limiting. 
处理声音的动态范围。 换言之，低音，高音和限制。

**Device type 设备类型**
Defines the headset type connected to the audio jack. If you cannot get the right device for a good bass tone, then select Common earphone.
定义连接到音频插孔的耳机类型。 如果您无法获得合适的设备来获得良好的低音，请选择通用耳机。

**Dynamic bass strength 动态低音强度**
Defines the average dynamic bass. The greater the stronger bass.
定义平均动态低音。 该值越大，低音越强。

### 电子管模拟器（6N1J）
This option defines whether to enable tube simulator effect. Tube simulator uses a simplified mathematical simulation of a tube effect.
该选项定义是否启用电子管模拟器效果。 电子管模拟器使用电子管效果的简化数学模拟。（*拗口*）

If turned on, it will greatly reduce high-frequency odd harmonic distortions, while it increases even-order harmonic distortions of tube simulators
如果打开，它将大大减少高频奇次谐波失真，同时增加电子管模拟器的偶次谐波失真。

### VIPER 低音
ViPER bass is a substitution for XHiFi’s Audio Reconstruction. It processes bass boost at lower frequencies
ViPER低音代替了XHiFi的音频重建。 在较低频率下处理低音增强

**Bass mode 低音处理模式**
Defines the bass mode. Natural bass is alike ViPER XHiFi’s Lo Contour, pure bass+ gives clean bass and subwoofer gives huge bass.
定义低音模式。 自然低音类似于 ViPER XHiFi 的 Lo Contour，醇低音+ 产生干净的低音，低音炮产生重低音。

**Bass frequency 低音频点**
Defines the bass cut-off frequency
定义低音截止频率

**Bass gain 低音增益**
Defines the volume of ViPER bass
定义 ViPER 低音的音量

### VIPER 清晰度
ViPER clarity is a substitution for XHiFi’s Audio Reconstruction. It adds clarity to the audio.
ViPER清晰度可替代XHiFi的音频重建。 它增加了音频的清晰度。

**Clarity mode 清晰度处理模式**
Defines the clarity mode. Natural has high vocal and treble, Ozone+ offers clean clarity and XHiFi is alike V4A XHiFi’s Hi Clarity.
定义清晰度模式。 天然的人声和高音高，醇氧+ 提供清晰的音质，XHiFi 就像 V4A XHiFi 的 Hi Clarity（高清晰度）。

**Clarity gain 清晰度（增益）**
Defines the volume of ViPER clarity
定义 ViPER 清晰度的量

### 听觉保护
Protects auditory system
保护听觉系统

Level 效果级别
Strength of Binaural protection
保护双耳的程度

### AnalogX
This option defines whether to enable a field effect transistor based amplifier effect.
此选项定义是否启用基于场效应晶体管的放大器效果。

AnalogX uses a simplified mathematical simulation of a field effect transistor.
AnalogX使用场效应晶体管的简化数学模拟。
