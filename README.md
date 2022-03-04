#include<stdio.h>
#include<math.h>

int main() {

	int a ;//=不表示相等。表示赋值
	int b ;
	int c ;

	printf("请输入一元二次方程中a b c的值；");
	scanf_s("%d %d %d", &a, &b, &c);
	

	int delta;//delta存放的是 b*b-4*a*c
	float x1, x2;//存放一元二次方程的两个解

	delta = b * b - 4 * a * c;

	if (delta > 0) 
	{
		x1 = (-b + sqrt(delta)) / (2 * a);
		x2 = (-b - sqrt(delta)) / (2 * a);  
		printf("该一元二次方程有两个解，x1 = %f,x2 = %f\n", x1, x2);

	}  
	else if (delta == 0)
	{
		x1 = (-b + sqrt(delta)) / (2 * a);
		x2 = x1;//两值相等，右边赋给左边+
	    printf("该一元二次方程有一个解，x1 = x2 = %f\n", x1);//这里不需要后面写x2  
	}
	else 
	{
		printf("该一元二次方程无解");	

	}

