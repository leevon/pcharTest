一个简单的C语言字符串操作测试方法.
=====
一个项目中的一部分，项目中需要通过配置灵活实现对一个字符串数组中的字符串实现叠加、逻辑、截取等操作。

字符前面如果不加＆代表的是字符串数组的下标，如果加＆代表的是当前的字符。add[1|2] ife[1|2|3|4] sub[1|2|3]

=====
eg:

char *srcStr[8] = {"vince_lee", "jay_", "chou", "jay_chou", "jay_chou", "23", "24", "25"};
char des[80] = {0};

mygetstr(des, "add[1|2]", srcStr);
des 的值: jay_chou


mygetstr(des, "ife[3|4|5|6]", srcStr);
des: 23

mygetstr(des, "sub[3|4|4]", srcStr);
des: chou



mygetstr(des, "ife[0|&vince_lee|1|2]", srcStr);
des: jay_


mygetstr(des, "ife[0|&vince_lee|&1|&2]", srcStr);
des: 1
