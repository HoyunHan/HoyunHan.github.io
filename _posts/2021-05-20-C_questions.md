---
layout: single
title: "C 수행평가"
toc: true
toc_sticky: true
toc_label: "main table of contents"
categories: "형성평가"
---

### 01. 사주보기 
![c_96p](/assets/images/c_96p.jpg)
~~~c
  #include <stdio.h>

int main(void) {
int year, month, day, result;
  printf("출생 연도, 달, 일을 차례로 입력하시오: ");
  scanf("%d %d %d", &year, &month, &day);
  result =(year - month + day)%10;
  if (result == 0)
  printf("대박\n");
  else
  printf("그럭저럭\n");
return 0;
}
~~~

### 02. 터널 통과
![c_98p](/assets/images/c_98p.jpg)
  ~~~c
  #include <stdio.h>

int main(void) {
int a, b, c, car=170;
  printf("터널의 높이를 차례로 세 개 입력하시오(cm): ");
  scanf("%d %d %d", &a, &b, &c);
  if(car >= a)
  printf("a(%dcm)에서 충돌\n", a);
  else if(car >= b)
  printf("b(%dcm)에서 충돌\n", b);
  else if(car >= c)
  printf("c(%dcm)에서 충돌\n", c);
  else
  printf("무사통과\n");
return 0;
}
~~~

### 03. 월별 날짜수
![c_100p](/assets/images/c_100p.PNG)
~~~c
  #include <stdio.h>

int main(void) {
  int y, m;
  printf("원하는 연도와 달을 차례로 입력하시오: ");
  scanf("%d %d", &y, &m);
  printf("%d년 %d월의 마지막 날은 ", y, m);
  if (m ==1 || m ==3 || m ==5 || m ==7 || m ==8 || m ==10  ||  m ==12 )
  printf("31일");
  else if (m ==4 || m ==6 || m ==9 || m ==11)
  printf("30일");
  else 
  {
    if ((y%4 == 0 && y%100 !=0) || y%400 ==0)
    printf("29일");
    else
    printf("28일");
  }
  return 0;
}
~~~

### 04. 30분 전 시간
![c_102p](/assets/images/c_102p.PNG)
~~~c
  #include <stdio.h>

int main(void) {
    int h, m;
  printf("시간과 분을 차례로 입력하시오: ");
  scanf("%d %d", &h, &m);
  if (m >= 30)
  printf("30분 전의 시각은 %d시 %d분입니다", h, m-30);
  else 
  {
    if (h == 0)
    printf("30분 전의 시각은 23시 %d분입니다", m+30);
    else
    printf("30분 전의 시각은 %d시 %d분입니다", h-1, m+30);
  }
  return 0;
}
~~~

### 05. 도어락
![doorlock](/assets/images/doorlock.PNG)
~~~c
  #include <stdio.h>

int main(void) {
 int rightkey = 24680, key, choose;
double rightjimun = 1.2345678, jimun;
char rightIC = 'c', IC;
 
printf(">>> 장치 선택: ");
scanf("%d", &choose);
 
if (choose  == 1)
{
 printf("IC를 입력하시오: ");
 scanf("%c", &IC);
}
else if (choose == 2)
{
 printf("비밀번호를 입력하시오: ");
 scanf("%d", &key);
}
else
{
 printf("지문을 입력하시오: \n");
 scanf("%lf", &jimun);
}
 
if((jimun == rightjimun) || (key == rightkey) || (IC == rightIC))
printf("문 열림");
else
printf("디리릭!디리릭!");
 
 return 0;
}
~~~

### 06. 가위바위보
![roscipa](/assets/images/roscipa.PNG)
~~~c
  #include <stdio.h>

int main(void) {
 char rsp, com_rsp='s';
 printf("r, s, p 중 하나를 입력하시오: ");
 scanf("%c", &rsp);
 if (rsp == com_rsp)
 printf("비겼다");
 else if ((rsp == 'r' && com_rsp == 's') || (rsp == 's' && com_rsp == 'p') || (rsp == 'p' && com_rsp == 'r'))
 printf("이겼다");
 else
 printf("졌다");
 return 0;
}
~~~

