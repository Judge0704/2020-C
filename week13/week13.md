## 利用Prossessing做按下滑鼠變顏色 且案幾次數字就是幾次
```C
void setup(){//只做一次設定
  size(1024, 400);
}
void draw(){
  if(mousePressed)background(255,255,0);//按下滑鼠後的背景顏色
  else background(0,0,255);//沒按時的背景顏色
  textSize(50);//文字大小
  text( a, 100,100);//a文字位置
}
int a=0;
void mousePressed(){//按下滑鼠會呼叫這個函數
  a++;
}
```
