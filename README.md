# Task: 3 LEDs - 3 Buttons

#### Purpose of the task :

``` 

يهدف هذا المشروع إلى تصميم دائرة إلكترونية بسيطة 
باستخدام لوحة اردوينو ، يتم من خلالها التحكم بثلاثة مصابيح (ليد) عبر ثلاثة أزرار .
يعتمد المشروع على مبدأ التبديل ؛
حيث يتم تشغيل المصباح عند الضغط على الزر لأول مرة، وإطفاؤه عند الضغط مرة أخرى.
ويهدف المشروع إلى تنمية المهارات الأساسية في برمجة المتحكمات الدقيقة، 
وفهم كيفية التعامل مع المدخلات والمخرجات الرقمية، 
بالإضافة إلى تعزيز الفهم العملي لأساسيات الدوائر الإلكترونية والتعامل مع إشارات الضغط.
```
#### Project Preview 
<img src= "https://github.com/user-attachments/assets/52c09654-8d52-41bb-98a0-2c5396e84982" width="500" hight="500">


#### Code :
```
int button1 = 2;
int button2 = 3;
int button3 = 4;

int led1 = 8;
int led2 = 9;
int led3 = 10;

bool led1State = false;
bool led2State = false;
bool led3State = false;

bool lastButton1 = LOW;
bool lastButton2 = LOW;
bool lastButton3 = LOW;

void setup() {
  pinMode(button1, INPUT);
  pinMode(button2, INPUT);
  pinMode(button3, INPUT);

  pinMode(led1, OUTPUT);
  pinMode(led2, OUTPUT);
  pinMode(led3, OUTPUT);
}

void loop() {
  bool nowButton1 = digitalRead(button1);
  bool nowButton2 = digitalRead(button2);
  bool nowButton3 = digitalRead(button3);

  if (nowButton1 == HIGH && lastButton1 == LOW) {
    led1State = !led1State;
    digitalWrite(led1, led1State);
    delay(200);
  }
  lastButton1 = nowButton1;

  if (nowButton2 == HIGH && lastButton2 == LOW) {
    led2State = !led2State;
    digitalWrite(led2, led2State);
    delay(200);
  }
  lastButton2 = nowButton2;

  if (nowButton3 == HIGH && lastButton3 == LOW) {
    led3State = !led3State;
    digitalWrite(led3, led3State);
    delay(200);
  }
  lastButton3 = nowButton3;
}

```

### Link of the Project on Tinkercad
[Tinkercad](https://www.tinkercad.com/things/lbVPt0b9QpI-cool-snaget-lappi?sharecode=DPwAyhGEEWpVylFeTHl-gLt83q1yfqTiHcioFM8MUBo) 
