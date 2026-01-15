# ДЗ к работе 13
## Условие задачи

печатает слова с чётным числом букв

   
### Блок-схема
<img width="251" height="671" alt="image" src="https://github.com/user-attachments/assets/72161cd6-218a-489f-a4e8-cd2a99b1bf9a" />






## 2. Реализация программы

```
#define _CRT_SECURE_NO_WARNINGS 
#include <locale.h>
#include <stdio.h>
#include <math.h>
#include <stdlib.h>
#include <string.h>

int main()
{
	SetConsoleCP(1251);
	SetConsoleOutputCP(1251);
	char str[255];
	puts("Введите предложение: ");
	fgets(str, sizeof(str), stdin);
	str[strcspn(str, "\n")] = '\0';

	char* word = strtok(str, " ");
	while (word != NULL)
	{
		int len = strlen(word);
		if (len % 2 == 0)
		{
			printf("%s\n", word);
		}
		word = strtok(NULL, " ");
	}
}
```


## 3. Результаты работы программы

```
Напишите предложение:
Введите предложение:
пр прр пррр прррр ыф
пр
пррр
ыф
```


<img width="823" height="250" alt="image" src="https://github.com/user-attachments/assets/ca8be067-7f96-4531-8d8f-82b98a8d70a6" />


