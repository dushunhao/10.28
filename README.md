#define _CRT_SECURE_NO_WARNINGS 1

#include<stdio.h>

#include<math.h>

int main()

{

	int count = 0;
  
	int i = 0;
  
	for (i = 101; i <= 200; i+=2)
  
	{
  
		int j = 0;
    
		int flag = 1;
    
		for (j = 2; j <= sqrt(i); j++)
    
		{
    
			if (i%j == 0)
      
			{
      
				flag = 0;
        
				break;
        
			}
      
		}
    
		if (flag == 1)
    
		{
    
			
			printf("%d ", i);//素数
      
            count++;
            
		}
    
		
	}
  
	printf("\ncount=%d\n", count);
  
	return 0;
  
}


int main()

{

flag:

	printf("hehe\n");
  
	printf("hehe\n");
  
	goto flag;
  
	return 0;
  
}




//关机程序

//只要运行起来，电脑就在1分钟内关机，如果输入：我是猪，就取消关机！

//shutdown -s -t 60 关机 时间 60s

//shutdown -a    取消关机



#include<stdlib.h>

#include<string.h>

int main()

{

	//关机
  
	//c语言函数：system（）—执行系统命令
  
	char input[20] = { 0 };
  
	system("shutdown -s -t 60");//stdlib.h
  

again:

	printf("请注意，你的电脑将在一分钟内关机，如果输入：我是猪，就取消关机\n");
  
	scanf("%s", input);
  
	if (strcmp(input,"我是猪") == 0)//两个字符串不能使用==，应该使用strcmp() string.h
  
	{
  
		system("shutdown -a");
    
	}
  
	else
  
	{
  
		goto again;
    
	}
  
	return 0;
  
}


#include<stdlib.h>

#include<string.h>

int main()

{

	//关机
  
	//c语言函数：system（）—执行系统命令
  
	char input[20] = { 0 };
  
	system("shutdown -s -t 60");//stdlib.h
  
	while (1)
  
	{
  
		printf("请注意，你的电脑将在一分钟内关机，如果输入：我是猪，就取消关机\n");
    
		scanf("%s", input);
    
		if (strcmp(input, "我是猪") == 0)//两个字符串不能使用==，应该使用strcmp() string.h
    
		{
    
			system("shutdown -a");
      
			break;
      
		}
    
    
	}
  
	return 0;
  
}
