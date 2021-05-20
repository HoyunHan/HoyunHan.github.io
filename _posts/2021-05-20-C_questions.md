---
layout: single
title: "C 수행평가"
toc: true
toc_sticky: true
toc_label: "main table of contents"
categories: "형성평가"
---

### 01. 사주보기
![c 96p ] (/assets/images/c 96p .jpg)
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
![c 98p] (/assets/images/c 98p.jpg)
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
