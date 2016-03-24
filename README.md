# AndroidLab
Android 实验室：模拟算法的运行轨迹，

##TODO
1、实现一个通用的图形库<br>
2、9大排序算法的实现，拼接图形库<br>
3、自定义算法拼接图形库<br>
4、时间复杂度分析显示<br>

##用法
```xml
<coderoom.jomeslu_lib.graphicalview
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
```
## Android 博客周刊
请关注[Android博客周刊](http://www.androidblog.cn/) 。优质、精简Android博客周刊。每周一准时更新。
