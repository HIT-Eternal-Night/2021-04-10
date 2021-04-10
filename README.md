# 2021-04-10
学习文件！C语言快要学完了！

格式化的输入输出问题：
·printf
%[flags][width][.prec][hlL]type
·scanf
%[flag]type

#include<stdio.h>

int main(int argc,char const *argv[])
{
  printf("%+9d#\n",123);
	printf("%+9d#\n",-123);

	printf("%+09d#\n",123);
	printf("%+09d#\n",-123);

	printf("%-9d#\n",123);
	printf("%-9d#\n",-123);

	printf("%-+9d#\n",-123);
  printf("%-+9d#\n", 123);

  printf("%+-9d#\n",-123);
  printf("%+-9d#\n", 123);

  printf("%*d#\n",9,123);
  printf("%9.2f#\n",123.0);
	printf("%*.*f#\n",9,2,123.0);
	
	return 0; 
}
输出结果如下：
     +123#
     -123#
+00000123#
-00000123#
123      #
-123     #
-123     #
+123     #
-123     #
+123     #
      123#
   123.00#
   123.00#
总结：
printf里
-为左对齐，+表示输出正号或负号
* 表示读入字符，特别适合用变量来控制输出的位宽
0补前不补后
