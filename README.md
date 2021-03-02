# ARDUINO-NO9
這次的題目是使用七段LED顯示器<p>
重複播放從1到9的數字<p>
程式內容如下<p>
```C++
  int a[10][7] = {{1,1,1,1,1,1,0},
                {0,1,1,0,0,0,0},
                {1,1,0,1,1,0,1},
                {1,1,1,1,0,0,1},
                {0,1,1,0,0,1,1},
                {1,0,1,1,0,1,1},
                {0,0,1,1,1,1,1},
                {1,1,1,0,0,1,0},
                {1,1,1,1,1,1,1},
                {1,1,1,0,0,1,1}
                };
void setup() {
  // put your setup code here, to run once:
  for(int i = 2 ;i<13;i++)
    pinMode(i,OUTPUT);
}

void loop() {
  // put your main code here, to run repeatedly:
  digitalWrite(9,HIGH);
  for(int j =0;j<10;j++)
    { 
      for (int i = 2 ; i<9;i++)
        digitalWrite(i,a[j][i-2]);
      delay(500);
    }
}
```
----------------------
成品如下
![image](https://github.com/qasx920624/ARDUINO-NO9/blob/main/627E1CB5-1A03-4A92-8330-493A94DB3110.jpeg)
-----------------------
第二題是控制兩個七段LED顯示器同時發亮<p>
程式內容如下
c++```
 int a[10][7] = {{1,1,1,1,1,1,0},
                {0,1,1,0,0,0,0},
                {1,1,0,1,1,0,1},
                {1,1,1,1,0,0,1},
                {0,1,1,0,0,1,1},
                {1,0,1,1,0,1,1},
                {0,0,1,1,1,1,1},
                {1,1,1,0,0,1,0},
                {1,1,1,1,1,1,1},
                {1,1,1,0,0,1,1}};              
int t[4] = {0,1,
            1,0};
float c;
void setup() {
  // put your setup code here, to run once:
  for(int i = 2 ;i<13;i++)
    pinMode(i,OUTPUT);
    c = millis();
}
int d[2] ={9,4};
void loop() {
  // put your main code here, to run repeatedly:

  for (int j = 0;j<2;j++)
    {
      digitalWrite(9,t[j+2]);   
      digitalWrite(10,t[j]);
      
      
      for(int i = 2;i<9;i++)
        {
          digitalWrite(i,a[d[j]][i-2]);
        }
        delay(5);
    }
}```
--------------
成品如下
![image](https://github.com/qasx920624/ARDUINO-NO9/blob/main/156112143_265898575015081_7421873842532701171_n.jpg)
