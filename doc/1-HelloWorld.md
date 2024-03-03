# Hello World

```c
case 'x': {
  int value = va_arg(vargs, int);
  for (int i = 7; i >= 0; i--) {
      int nibble = (value >> (i * 4)) & 0xf;
      putchar("0123456789abcdef"[nibble]);
  }
}
```

16進数表記を行う。ビットでは4 bitで16進数の一桁であることを念頭に置く。
32 bitのOSなので最上位は32～29 bit。
ゆえに、28 bit分ずらして、`1111 = 0xf`の論理積を取り値を抽出
