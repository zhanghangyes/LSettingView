# LSettingView
设置界面条目封装，同时包含：

 - 设置左侧图标
 - 设置左侧文字
 - 设置右侧图标
 - 设置右侧图标是否显示
 - 设置右侧为复选框样式
 - 设置右侧为开关模式

### 运行效果：
![效果1](http://o9w936rbz.bkt.clouddn.com/github/img/LSettingView/Screenshot_20170331-144331.png?imageView2/0/w/500/h/1200)
![效果2](http://o9w936rbz.bkt.clouddn.com/github/img/LSettingView/Screenshot_20170331-144350.png?imageView2/0/w/500/h/1200)
![效果3](http://o9w936rbz.bkt.clouddn.com/github/img/LSettingView/Screenshot_20170331-144358.png?imageView2/0/w/500/h/1200)

### 快速使用
#### 1. 添加依赖

    compile 'com.leon:lsettingviewlibrary:1.0'
    
#### 2. 在布局文件中引用

    <com.leon.lib.settingview.LSettingItem
        xmlns:app="http://schemas.android.com/apk/res-auto"
        android:id="@+id/item_one"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        leon:leftIcon="@drawable/history"
        leon:leftText="我的消息"/>
                
#### 3. 添加单击事件处理

    LSettingItem mSettingItemOne = (LSettingItem) findViewById(R.id.item_one);
    mSettingItemOne.setmOnLSettingItemClick(new LSettingItem.OnLSettingItemClick() {
            @Override
            public void click() {
                Toast.makeText(getApplicationContext(), "我的消息", Toast.LENGTH_SHORT).show();
            }
        });
    
### 自定义属性
#### 方法说明
| 属性        | 说明   |类型   |
| --------   | --------- |--------- |
| leftText |左侧文字|string|
| leftIcon |左侧图标|integer|
| rightIcon |右侧图标|integer|
| textSize |左侧文字大小|dimension|
| textColor |左侧文字颜色|color|
| isShowUnderLine |是否显示底部分割线|boolean|
| rightStyle |右侧图标风格|enum|


#### 右侧图标风格
 
 - iconShow   显示图标
 - iconHide   隐藏图标
 - iconCheck  显示复选框
 - iconSwitch 显示切换开关

