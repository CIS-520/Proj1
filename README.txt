CIS 520 - Proj 0 - Paula Mendez

First, to know the changes to be done, I ran `grep –r alarm-multiple *` - the relevant files needed modifications are:
-> pintos/src/tests/threads/tests.c
	added `{"alarm-mega", test_alarm_mega},`

-> pintos/src/tests/threads/Make.tests
	added `alarm-mega` to the test names

-> pintos/src/tests/threads/Rubric.alarm;
	added `alarm-mega` to the list

I also did `grep -r test_alarm_multiple` and modified:
-> pintos/src/tests/threads/alarm-wait.c
	added
	`test_alarm_mega (void)
	{
	  test_sleep (5, 70);
	}`

-> pintos/src/tests/threads/tests.h
	added `extern test_func test_alarm_mega;`

after all the changes I made sure that all the dependencies from `alarm_multiple` are applied to `alarm-mega` 

I did 1.2 again
	ran `make clean` and `make` on pintos/src/threads


