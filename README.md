
## Android-PickerView

   这是一个基于Bigkoo/Android-PickerView选择控件基础上,添加日期是否显示星期数功能
   ![TimePickerWeek.gif](https://github.com/More-Stronger/Android-PickerView/blob/master/preview/timepicker_week.gif)
   
### **如何使用：**

#### Android-PickerView 库使用示例：

#### 1.Add the JitPack repository to your build file
      allprojects {
         repositories {
			   ...
			   maven { url 'https://jitpack.io' }
		   }
	   }
      
#### 2. Add the dependency
	   dependencies {
	          implementation 'com.github.More-Stronger.Android-PickerView:pickerview:v2.0.1'
	   }
      
#### 3.时间选择器使用参数
      new TimePickerBuilder(this, new OnTimeSelectListener() {
            @Override
            public void onTimeSelect(Date date,View v) {//选中事件回调
                tvTime.setText(getTime(date));
            }
        })
                .setDayIsShowWeek(true)//显示日期星期数  默认为不显示
                .setType(new boolean[]{true, true, true, true, true, true})// 默认全部显示          
                .setCancelText("Cancel")//取消按钮文字
                .setSubmitText("Sure")//确认按钮文字
                .setContentSize(18)//滚轮文字大小
                .setTitleSize(20)//标题文字大小
                .setTitleText("Title")//标题文字
                .setOutSideCancelable(false)//点击屏幕，点在控件外部范围时，是否取消显示
                .isCyclic(true)//是否循环滚动
                .setTitleColor(Color.BLACK)//标题文字颜色
                .setSubmitColor(Color.BLUE)//确定按钮文字颜色
                .setCancelColor(Color.BLUE)//取消按钮文字颜色
                .setTitleBgColor(0xFF666666)//标题背景颜色 Night mode
                .setBgColor(0xFF333333)//滚轮背景颜色 Night mode
                .setDate(selectedDate)// 如果不设置的话，默认是系统时间*/
                .setRangDate(startDate,endDate)//起始终止年月日设定
                .setLabel("年","月","日","时","分","秒")//默认设置为年月日时分秒
                .isCenterLabel(false) //是否只显示中间选中项的label文字，false则每项item全部都带有label。
                .isDialog(true)//是否显示为对话框样式
                .build();
                
		
#### ==========华丽的分割线，原作者Github链接如下==========
#### https://github.com/Bigkoo/Android-PickerView

![TimePicker.gif](https://github.com/More-Stronger/Android-PickerView/blob/master/preview/timepicker.gif)
![TimePickerNight.gif](https://github.com/More-Stronger/Android-PickerView/blob/master/preview/timepicker_night.gif)
![lunar.gif](https://github.com/More-Stronger/Android-PickerView/blob/master/preview/lunar.gif)
![XOffset.png](https://github.com/More-Stronger/Android-PickerView/blob/master/preview/Screen%20Shot%202017-11-09%20at%204.25.02%20PM.png)
![Province.gif](https://github.com/More-Stronger/Android-PickerView/blob/master/preview/JsonData.gif)
![CustomLayout.gif](https://github.com/More-Stronger/Android-PickerView/blob/master/preview/CustomLayout.gif)

