# Домашнее задание к занятию «Основы Git»

### Цель задания

В результате выполнения задания вы:

* научитесь работать с Git, как с распределённой системой контроля версий; 
* сможете создавать и настраивать репозиторий для работы в GitHub, GitLab и Bitbucket; 
* попрактикуетесь работать с тегами;
* поработаете с Git при помощи визуального редактора.

### Чеклист готовности к домашнему заданию

1. Установлена консольная утилита для работы с Git.
2. Есть возможность зарегистрироваться на GitHub, GitLab.
3. Регистрация на Bitbucket не является обязательной. 


### Инструкция к заданию

1. В личном кабинете отправьте на проверку ссылки на ваши репозитории.
2. Любые вопросы по решению задач задавайте в чате учебной группы.

------

## Задание 1. Знакомимся с GitLab и Bitbucket 

ТАК КАК В РОССИИ САНКЦИИ, Я НЕ СМОГ ЗАРЕГИСТРИРОВАТЬСЯ В GITLUB. нУЖНО ПРИВЕЗАТЬ НОМЕР ТЕЛЕФОНА В АККАУНТУ ПРИ РЕГИСТРАЦИИ, НО РОССИИ ТАМ НЕТ, ПОЭТОМУ И ПРИВЯЗЫВАТЬ НЕЧЕГО. РЕШИЛ СДЕЛАТЬ ДЗ В GITHUB.  

### GitHub

1. Создадим аккаунт в GitHub, если у вас его ещё нет.
2. После регистрации или авторизации в GitHub создайте новый репозиторий, нажав на ссылку `Create a projet`. 
Желательно назвать также, как и в GitHub — `devops-netology` и `visibility level`, выбрать `Public`.
3. Галочку `Initialize repository with a README` лучше не ставить, чтобы не пришлось разрешать конфликты.
   
   ![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/c83187fb-de8a-4018-86b7-729b857037c0)
   
4. Перейдите на страницу созданного вами репозитория, URL будет примерно такой:
https://github.com/YOUR_LOGIN/devops-netology. Изучите предлагаемые варианты для начала работы в репозитории в секции
`Command line instructions`.

![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/8656e5ee-68e6-438e-af9d-dec4b0b8577e)

6. Запомните вывод команды `git remote -v`.
   
 ![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/944274a0-a377-4073-9027-4502c026c00d)

7. Из-за того, что это будет наш дополнительный репозиторий, ни один вариант из перечисленных в инструкции (на странице 
вновь созданного репозитория) нам не подходит. Поэтому добавляем этот репозиторий, как дополнительный `remote`, к созданному
репозиторию в рамках предыдущего домашнего задания:
`git remote add gitlab https://gitlab.com/YOUR_LOGIN/devops-netology.git`.

![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/b7f78012-071e-4914-acab-7b7170c27af9)
![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/4893097c-504c-412f-959d-ac781e6f9237)

8. Отправьте изменения в новый удалённый репозиторий `git push -u gitlab main`.

![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/0b7978de-a610-438b-8124-499ced026545)
![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/1eeb433b-5a68-4d8f-8deb-1de8e6cefa37)

7. Обратите внимание, как изменился результат работы команды `git remote -v`.

![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/cb10a513-bf33-454f-8976-dd932093cb7b)

https://github.com/bezymel/visibility-level
