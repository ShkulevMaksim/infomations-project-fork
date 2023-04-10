# Документация для программного кода игры "Угадай число"
Данная программа представляет собой игру "Угадай число". Игрок должен угадать число, загаданное программой, в определенном диапазоне, с ограниченным количеством попыток. Игрок может делать ставки и выигрывать или проигрывать деньги.

***



+ Функция "get_attempts(char*)" запрашивает у пользователя количество попыток.
```
	float get_attempts(char* name) {
	float attempts;
	do {
		printf("%s введите количество попыток: ", name);
		if (scanf("%f", &attempts) != 1 || attempts < 1) {
			printf("Ошибочный формат количества попыток! Повторите попытку!\n");
		}
	} while (attempts < 1);
	return attempts;
	}
```
+ Функция "update_score(int, float, int, float, float)" обновляет баланс игрока в зависимости от исхода игры.
```
	int update_score(int boo, float score, int g_number, float win, float bet) {
	if (boo == 0) {
		printf("--------------------------------------\n");
		printf("----Попытки закончились, Вы проиграли.\n");
		printf("----Число которое мы загадали -- %d\n", g_number);
		score -= bet;
		printf("----На вашем счету доступно %.2f$\n", score);
	}else {
		printf("--------------------------------------\n");
		printf("---------Вы выйграли %.2f$-----------\n", win);
		score = score - bet + win;
		printf("----На вашем счету доступно %.2f$----\n", score);
		printf("--------------------------------------\n");
	}
	return score;
	}
```

***

![Пример работы программы](https://sun9-32.userapi.com/impg/7q_Fzu-XeKHpR2wUXLcxalzIP2qUy3KbxzDFPQ/9AhNZsZINYs.jpg?size=1062x527&quality=96&sign=e45c575e6ec7ed736f94b31b5f780448&type=album)

> Пример работы программы.

[Ссылка на второй файл](./second_file)
