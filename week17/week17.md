## 打字練習
```C
void setup(){
  size(400,200);
  textSize(40);
}
String line=" ";//空白
String []Q={"hello","world","other"};//陣列裡面的英文 先舉例三個 如果要更多就全部打上去
int Qi=0;
void draw(){
  background(0);
  text("Score: "+score,100,50);
  text("Q: "+Q[Qi],100,100);
  text("A: "+line,100,150);
}
int score=0;
void keyPressed(){
  int len=line.length();
  if(key>='a' && key<='z')line+=key;
  if(key>='A' && key<='Z')line+=key;
  if(key == BACKSPACE && len>0)line=line.substring(0,len-1);
  if(key ==ENTER){
    if(line.equals(Q[Qi])==true){
      score++;//當答對的時候分數+1
      Qi++;   //換成Q[]陣列的下一題
      line="";
    }
  }
}
```
  
   
