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
