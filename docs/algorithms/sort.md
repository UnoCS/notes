# 排序

## 选择排序

```java title="An example"
import java.util.Arrays;

public class Main {
    public static void main(String[] args) {
        int[] array = {1, 5, 3, 6, 2, 10, 9, 4, 11, 0};
        int min_pos, tmp;
        for(int i=0; i<10; i=i+1){
            min_pos = i;
            for(int j=i+1; j<10; j=j+1){
                if(array[j] < array[min_pos]){
                    min_pos = j;
                }
            }
            tmp = array[i];
            array[i] = array[min_pos];
            array[min_pos] = tmp;
        }
        System.out.println(Arrays.toString(array));
    }
}
```

## 插入排序

## 合并排序

## 快速排序

