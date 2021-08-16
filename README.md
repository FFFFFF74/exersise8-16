# exersise8-16
#include<stdio.h>
#include<string.h>
int main() {
    int i = 0, j = 0;
    char str1[20], str2[20], str[50];
    memset(str, '\0', sizeof(char)*50);
    scanf("%s", str1);
    scanf("%s", str2);
    while (str1[i] != 0) {
        str[j++] = str1[i++];
    }
    i = 0;
    while (str2[i] != 0) {
        str[j++] = str2[i++];
    }
    printf("%s", str);
    return 0;
}
#define _CRT_SECURE_NO_WARNINGS #include<stdio.h>
#include<stdio.h>
#include<string.h>

//int main()
//{
//	char s1[80], s2[40]; /*s2连接在s1后面，s1应足够大*/
//	int i = 0;
//	int j = 0;
//	scanf("%s",s1); /*输入串s1*/
//	scanf("%s", s2); /*输入串s2*/
//	while (s1[i] != '\0')
//		i++; /*i指向s1串末尾的'\0'处*/
//	while (s2[j] != '\0')
//		s1[i++] = s2[j++]; /*将s2串的各个字符放到s1串适当位置*/
//	s1[i] = '\0'; /*加结束标记*/
//	printf("%s\n", s1); /*显示连接后的串*/
//	return 0;
//}

char* my_strcat(char* p1, char* p2)
{
	int* ret = p1;
	while (*p1 != '\0')
	{
		p1++;
	}
	while (*p2 != '\0')
	{
		*p1 = *p2;
		p1++;
		p2++;
	}
	return ret;
}
int main()
{
	char arr1[40] = { 0 };
	char arr2[20] = { 0 };
	char* p = arr1;
	char* p1 = arr1;
	char* p2 = arr2;
	scanf("%s[^\n]", arr1);
	scanf("%s", arr2);
	
	printf("%s", my_strcat(arr1,arr2));
	return 0;
}	

////错误原因，主要是数据类型不对
// //用动态链表来做 不会呀！
//#include<stdio.h>
//void inputscore(float arr[], int n)
//{
//    for (int i = 0; i < n; i++)
//    {
//        scanf("%f[^ ]", &arr[i]);
//    }
//}
//
//float average(float arr[], int n)
//{
//    float sum = 0;
//    for (int i = 0; i < n; i++)
//    {
//        sum += arr[i];
//    }
//    return sum / n;
//}
//void bublltsort(float arr[], int n)
//{
//    float temp;
//    for (int i = 0; i < n - 1; i++)
//    {
//        for (int j = 0; j < i - 1; j++)
//        {
//            if (arr[j] < arr[j + 1])
//            {
//                temp = arr[j];
//                arr[j] = arr[j + 1];
//                arr[j + 1] = temp;
//            }
//        }
//    }
//}
//int main()
//{
//    float arr[100] = { 0 };
//    int n = 0;
//    float aver = 0;
//    float max = 0;
//    float min = 0;
//    scanf("%d", &n);
//    inputscore(arr, n);
//    aver = average(arr, n);
//    bublltsort(arr, n);
//    min = arr[n - 1];
//    max = arr[0];
//
//    printf("average = %.2f\n", aver);
//    printf("max = %.2f\n", max);
//    printf("min = %.2f\n", min);
//    return 0;
//}


//int main()
//{
//    int arr[10] = { 0 };
//    int n = 0;
//    scanf("%d", &n);
//    inputscore(arr, n);
//    for (int i = 0; i < n; i++)
//    {
//        printf("%d ", arr[i]);
//    }
//    return 0;
//}

//将俩个字符串连起来

//
//int main()
//{
//	char arr1[100] = { 0 };
//	char arr2[100] = { 0 };
//	char* pt1 = arr1;
//	char* pt2 = arr2;
//	while (*pt1 != '\0')
//	{
//		pt1++;
//	}
//	pt1++;
//
//}

//int main()
//{
//	char arr1[100] = "beijing_";
//	char arr2[] = "i will come";
//	strcat(arr1, arr2);
//	/*int len = strlen(arr1);
//	arr1[len] = '\0';*/
//	printf("%s", arr1);
//	return 0;
//}
//int main()
//{
//    int N;
//    float m, M;
//    scanf("%d %f\n", &N, &M);
//    for (int j = 0; j < N; j++)
//    {
//        scanf("%f", &m);
//        if (m < M)
//        {
//            printf("On Sale! %3.1f\n", m);
//        }
//    }
//    return 0;
//}


//输出俩个数乘积的值 的每一位数
//若输出的数加起来等于n的话，则停止输出

//数据放在数组中，可以依次运算
//循环，当count = n - 2时跳出循环


//int main()
//{
//    int a1, a2, n;
//    scanf("%d%d%d", &a1, &a2, &n);
//    int shu[20001] = { 0 }, tmp, dd = 1;
//    shu[0] = a1; shu[1] = a2;
//    for (int i = 0; i < n - 2; i++)
//    {
//        tmp = shu[i] * shu[i + 1];
//        if (tmp < 10) {
//            dd++;
//            shu[dd] = tmp;
//        }
//        else if (tmp < 100) {
//            shu[dd + 2] = tmp % 10;
//            shu[dd + 1] = tmp / 10 % 10;
//            dd = dd + 2;
//        }
//        else if (tmp < 1000)
//        {
//            shu[dd + 3] = tmp % 10;
//            shu[dd + 2] = tmp / 10 % 10;
//            shu[dd + 1] = tmp / 100 % 10;
//            dd = dd + 3;
//        }
//    }
//    for (int g = 0; g < n; g++)
//    {
//        printf("%d", shu[g]);
//        if (g < n - 1)printf(" ");
//    }
//    return 0;
//}


//int main()
//{
//	int a1, a2;
//	int n;
//	int temp;
//	int flag = 2;
//	int count = 0;
//	scanf("%d %d %d", &a1, &a2, &n);
//	printf("%d %d ",a1, a2);
//	while(count != n)
//	{
//		temp = a2;
//		flag = 2;
//		//输出的时候有问题
//		if (a1 * a2 > 10)
//			while (flag)
//			{
//				count--;
//				printf("%d ", (a1 * a2) / 10);
//				printf("%d ", (a1 * a2) % 10);
//				count += 2;
//			}
//			
//		else
//		{
//			printf("%d ", a1 * a2);
//			count++;
//		}
//			
//		a2 = (a1 *a2) % 10;
//		a1 = temp;
//	}
//	return 0;
//}







//void inputscore(float arr[], int n)
//{
//    for (int i = 0; i < n; i++)
//    {
//        scanf("%d", &arr[i]);
//    }
//}
//
//float average(float arr[], int n)
//{
//    float sum = 0;
//    for (int i = 0; i < n; i++)
//    {
//        sum += arr[i];
//    }
//    return sum / n;
//}
//void bublltsort(float arr[], int n)
//{
//    int temp;
//    for (int i = 0; i < n - 1; i++)
//    {
//        for (int j = 0; j < i - 1; j++)
//        {
//            if (arr[j] < arr[j + 1])
//            {
//                temp = arr[j];
//                arr[j] = arr[j + 1];
//                arr[j + 1] = temp;
//            }
//        }
//    }
//}
//int main()
//{
//    float arr[100] = { 0 };
//    int n = 0;
//    float aver = 0;
//    float max = 0;
//    float min = 0;
//    scanf("%d", &n);
//    inputscore(arr, n);
//    aver = average(arr, n);
//    bublltsort(arr, n);
//    max = arr[0];
//    min = arr[n - 1];
//    for(int i = 0;i<n)
//    printf("average = %d\n", aver);
//    printf("max = %d\n", max);
//    printf("min = %d\n", min);
//    return 0;
//}
