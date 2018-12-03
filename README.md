# DragFloatingActionButton
一个可以随处拖曳FloatingActionButton，边缘自动吸附，拖曳避免阻挡界面视图无法查看。

![image](https://github.com/wangfeng19930909/DragFloatingActionButton/blob/master/screenshot/1543217567144_video.gif)

使用步骤
=================================== 

step1:
-------

在gradle中直接引用

在你项目根目录的build.gradle中添加

	allprojects {
	
		repositories {
		
		...
		
		maven { url 'https://jitpack.io' }
		
		}
		
	}
   
step2:
-------

在module下的build.gradle中添加，由于库中使用的appcompat-v7是28.0.0，如果不一样则可能会冲突，所以在此添加exclude module: 'appcompat-v7'。

		dependencies {
		
	        	implementation ('com.github.wangfeng19930909:DragFloatingActionButton:v1.0.0'){
			
        			exclude module: 'appcompat-v7'
				
    			}
		
		}
		
step3:
-------

<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <com.barnettwong.dragfloatactionbuttonlibrary.view.DragFloatActionButton
        android:id="@+id/circle_button"
        android:layout_width="48dp"
        android:layout_height="48dp"
        android:layout_alignParentBottom="true"
        android:layout_alignParentRight="true"
        android:layout_marginBottom="20dp"
        android:layout_marginRight="20dp"
        android:clickable="true"
        android:src="@mipmap/tianjia" />

</RelativeLayout>

MIT License
=================================== 
Copyright 2017-2018, wangfeng19930909

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at http://www.apache.org/licenses/LICENSE-2.0
   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.
