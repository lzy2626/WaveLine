[![](https://jitpack.io/v/lzy2626/WaveLine.svg)](https://jitpack.io/#lzy2626/WaveLine)



### 前言
  项目中又语音录入文字的功能，需要一个动画效果。所以需要时间一个随音频大小而改变的波浪。是基于[A memory-friendly recording wave animation一款性能内存友好的录音波浪动画](https://github.com/Jay-Goo/WaveLineView)的基础上进行修改完成的。感谢这位大神，[原理讲解请看这里](https://github.com/Jay-Goo/WaveLineView/blob/master/blog.md)。
### 看一下效果图：

![GIF.gif](https://upload-images.jianshu.io/upload_images/11207183-274b47a8cac36088.gif?imageMogr2/auto-orient/strip%7CimageView2/2/w/410/format/webp)

### 使用方式：

###### Step 1. Add it in your root build.gradle at the end of repositories:
```
    allprojects { 
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
```

###### Step 2. Add the dependency

```
	dependencies {
	        implementation 'com.github.lzy2626:WaveLine:1.0'
	}
```
###### Step 3.xml
```
    <com.lzy.waveline.WaveLineView
        android:id="@+id/waveLineView"
        android:layout_width="match_parent"
        android:layout_height="200dp"
        app:wlvBackgroundColor="@android:color/white" />
```
###### Step 4.activity
```
  waveLineView = (WaveLineView) findViewById(R.id.waveLineView);
  waveLineView.startAnim();

//根据声音大小进行设置
 waveLineView.setVolume((int) db);
```