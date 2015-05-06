# Light-AudioPlayer
A Light AudioPlayer with HTML5, jQuery and CSS3.

[DEMO](http://laplayer.sinaapp.com/)&nbsp;&nbsp;|&nbsp;&nbsp;Music: Motto - Kana Nishino

##特点

###轻量级
整个插件在JS、CSS压缩后最小只有4KB

###快速响应
采用CSS3特性，自适应各种屏幕，使Light AudioPlayer在手机和平板上也能良好的运作

###触摸支持
你可以用光标，也可以用你的手指。每一个动作都有它的触摸事件的定义和功能

###适应能力
1. JavaScript被禁用？不用担心，浏览器中的内置播放器将代替工作
2. 音量按钮在有系统有音量控制组件时不可用（如iOS）
3. 当浏览器不支持`<audio>`元素或提供的音频文件时，将使用Quick Time, Windows Media Player来播放音频

###没有图片
全都是CSS做的，兄弟

###控制按钮
1. 基本的播放/暂停和播放进度控制
2. 音量微调与静音
3. **缓冲进度显示**

##如何使用
没什么特别的，只是采用了HTML5 `<audio>`标签的典型用法：

`<audio src="audio.wav" preload="auto" controls></audio>`

还不够屌？你可以加上自动播放(`autoplay`)与循环播放(`loop`)：

`<audio src="audio.wav" preload="auto" controls autoplay loop></audio>`

###浏览器兼容性
当前，audio 元素支持三种音频格式（via W3CSchool）：
<table>
<tr>
<th>&nbsp;</th>
<th style="width:16%;">IE 9</th>
<th style="width:16%;">Firefox 3.5</th>
<th style="width:16%;">Opera 10.5</th>
<th style="width:16%;">Chrome 3.0</th>
<th style="width:16%;">Safari 3.0</th>
</tr>

<tr>
<td>Ogg Vorbis</td>
<td>&nbsp;</td>
<td>&#8730;</td>
<td>&#8730;</td>
<td>&#8730;</td>
<td>&nbsp;</td>
</tr>

<tr>
<td>MP3</td>
<td>&#8730;</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&#8730;</td>
<td>&#8730;</td>
</tr>

<tr>
<td>Wav</td>
<td>&nbsp;</td>
<td>&#8730;</td>
<td>&#8730;</td>
<td>&nbsp;</td>
<td>&#8730;</td>
</tr>
</table>

**上表可以看出，没有一种格式是支持所有浏览器的**

所以，要尽可能支持更多的浏览器，你可以这样指定多个音频格式：

    <audio preload="auto" controls>
      <source src="audio.wav" />
      <source src="audio.mp3" />
      <source src="audio.ogg" />
    </audio>

###添加一波JS
呵呵哒。

    <audio src="audio.wav" preload="auto" controls></audio>
    <script src="jquery.js"></script>
    <script src="audioplayer.js"></script>
    <script>$( function() { $( 'audio' ).audioPlayer(); } );</script>
    
##更多高级用法、小魔术等待添加...
可以自己先研究下audioplayer.js哦。
