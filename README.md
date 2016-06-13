# AndroidLab
Android 实验室：模拟算法的运行轨迹，

##TODO
1、实现一个通用的图形库<br>
2、9大排序算法的实现，拼接图形库<br>
3、自定义算法拼接图形库<br>
4、时间复杂度分析显示<br>

##用法
```xml
<com.coderoom.jomeslu_lib.graphicalview
    android:id="@+id/videocontroller1"
    android:layout_width="match_parent"
    android:layout_height="200dp" />
```
##文档
优化后的冒泡排序
```java
public class Bubblesort implements Sortable {
    @Override
    public void sort(Comparable[] a) {
        for(int i=0;i<a.length-1;i++){
            boolean didSwap = flase;
            for(int j=0;j<a.length-1-i;j++){
                if(less(a[j+1],a[j])){
                    exch(a,j,j+1);
                    didSwap = true;
                }
            }
            if(!didSwap) return ;
        }
    }
}

public void preload(){
    MobVistaSDK sdk = MobVistaSDKFactory.getMobVistaSDK();
    Map<String,Object> preloadMap = new HashMap<String,Object>();
    preloadMap.put(MobVistaConstans.PROPERTIES_LAYOUT_TYPE, MobVistaConstans.LAYOUT_NATIVE);//广告样式
    preloadMap.put(MobVistaConstans.ID_FACE_BOOK_PLACEMENT, "1611993839047594_1614040148842963");//fbid  
    preloadMap.put(MobVistaConstans.ID_MY_TARGET_AD_UNITID, "6590");//MyTarget id
    preloadMap.put(MobVistaConstans.PREIMAGE,true);//设置为true为预加载图片
    preloadMap.put(MobVistaConstans.PROPERTIES_UNIT_ID, "12");//unit
     //请求广告category,一共有2种分类：game和app，category不是必传参数
    preloadMap.put(MobVistaConstans.PROPERTIES_API_REUQEST_CATEGORY,
                MobVistaConstans.API_REUQEST_CATEGORY_APP);
  //preloadMap.put(MobVistaConstans.PROPERTIES_API_REUQEST_CATEGORY,
  //                MobVistaConstans.API_REUQEST_CATEGORY_GAME)
    List<Template> list = new ArrayList<Template>();//为支持多模板需要添加的部分
    list.add(new Template(MobVistaConstans.TEMPLATE_BIG_IMG, 1));//支持大图模板，每次获取1条
    list.add(new Template(MobVistaConstans.TEMPLATE_MULTIPLE_IMG, 1));//支持多图模板，每次获取1条
    String nativeInfo =  MvNativeHandler.getTemplateString(list);//将native_info参数传入
    preloadMap.put(MobVistaConstans.NATIVE_INFO, nativeInfo);
    sdk.preload(preloadMap);
}
```
## Android 博客周刊
请关注[Android博客周刊](http://www.androidblog.cn/) 。优质、精简Android博客周刊。每周一准时更新。
