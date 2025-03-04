# Домашнее задание к занятию «Системы контроля версий»

### Цель задания

В результате выполнения задания вы: 

* научитесь подготоваливать новый репозиторий к работе;
* сохранять, перемещать и удалять файлы в системе контроля версий.  


### Чеклист готовности к домашнему заданию

1. Установлена консольная утилита для работы с Git.


### Инструкция к заданию

1. Домашнее задание выполните в GitHub-репозитории. 
2. В личном кабинете отправьте на проверку ссылку на ваш репозиторий с домашним заданием.
3. Любые вопросы по решению задач задавайте в чате учебной группы.


### Дополнительные материалы для выполнения задания

1. [GitHub](https://github.com/).
2. [Инструкция по установке Git](https://git-scm.com/downloads).
3. [Книга про  Git на русском языке](https://git-scm.com/book/ru/v2/) - рекомендуем к обязательному изучению главы 1-7.
   
   
------

## Задание 1. Создать и настроить репозиторий для дальнейшей работы на курсе

В рамках курса вы будете писать скрипты и создавать конфигурации для различных систем, которые необходимо сохранять для будущего использования. 
Сначала надо создать и настроить локальный репозиторий, после чего добавить удалённый репозиторий на GitHub.

### Создание репозитория и первого коммита

1. Зарегистрируйте аккаунт на [https://github.com/](https://github.com/). Если предпочитаете другое хранилище для репозитория, можно использовать его.
   
![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/5d4631f2-ea3c-4e41-bcb7-d43c2f890422)

3. Создайте публичный репозиторий, который будете использовать дальше на протяжении всего курса, желательное с названием `devops-netology`.
   Обязательно поставьте галочку `Initialize this repository with a README`. 

![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/347f4c70-d8b6-48db-b1aa-7659f5bbdc49)
    
4. Создайте [авторизационный токен](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token) для клонирования репозитория.

![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/d9ac6637-5a7c-4763-82f1-918880b58361)

6. Склонируйте репозиторий, используя протокол HTTPS (`git clone ...`).

![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/c972c283-350b-4220-82c2-00f2f5ea47ea)

8. Перейдите в каталог с клоном репозитория (`cd devops-netology`).

![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/03be9294-ada3-4c7b-810b-75f4a399696f)

9. Произведите первоначальную настройку Git, указав своё настоящее имя, чтобы нам было проще общаться, и email (`git config --global user.name` и `git config --global user.email johndoe@example.com`).

![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/ed19ef80-20e9-4201-ad97-4d3ff748d9b2)
  
10. Выполните команду `git status` и запомните результат.

![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/63a24e53-8bd2-4037-9d6b-0fe7fe22c557)
    
11. Отредактируйте файл `README.md` любым удобным способом, тем самым переведя файл в состояние `Modified`.
    
![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/73f4f3fe-5834-47d8-bbe0-9a9a00c10064)

13. Ещё раз выполните `git status` и продолжайте проверять вывод этой команды после каждого следующего шага.

![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/bc11ffba-b28b-4579-8ab9-f40e3c68b9f5)

15. Теперь посмотрите изменения в файле `README.md`, выполнив команды `git diff` и `git diff --staged`.

![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/a226c317-353e-4062-965f-a2cc3f55dd08)
    
17. Переведите файл в состояние `staged` (или, как говорят, просто добавьте файл в коммит) командой `git add README.md`.

![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/d60c93df-c7e2-4a3e-a180-c3a31deb48e7)
  
19. И ещё раз выполните команды `git diff` и `git diff --staged`. Поиграйте с изменениями и этими командами, чтобы чётко понять, что и когда они отображают.

![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/6bdb3192-85d2-450d-b91e-f13933bfc861)

21. Теперь можно сделать коммит `git commit -m 'First commit'`.
    
![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/b40eed43-d597-4b48-8655-d96bae8d902e)

23. И ещё раз посмотреть выводы команд `git status`, `git diff` и `git diff --staged`.

![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/d05d0d63-e097-4c51-bdcc-815899fde876)

### Создание файлов `.gitignore` и второго коммита

1. Создайте файл `.gitignore` (обратите внимание на точку в начале файла), проверьте его статус сразу после создания.

![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/1d2d8371-c9ad-414e-b230-08eba37b0381)

2. Добавьте файл `.gitignore` в следующий коммит (`git add...`).

![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/506cb298-74c9-48c7-a576-97e163d6148f)

3. На одном из следующих блоков вы будете изучать `Terraform`, давайте сразу создадим соотвествующий каталог `terraform` и внутри этого каталога — файл `.gitignore` по примеру: https://github.com/github/gitignore/blob/master/Terraform.gitignore. "ССЫЛКА БИТАЯ! НЕ ДЕЙСТВИТЕЛЬНА! ПО КРАЙНЕЙ МЕРЕ НА МОМЕНТ ВЫПОЛНЕНИЯ ДЗ!"

![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/d6853872-2b62-455a-9f8e-1d091552041c)

4. В файле `README.md` опишите своими словами, какие файлы будут проигнорированы в будущем благодаря добавленному `.gitignore`.

![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/d87dabb8-8d3b-4f05-b288-30a8148561e4)

5. Закоммитьте все новые и изменённые файлы. Комментарий к коммиту должен быть `Added gitignore`.

![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/26bbcc14-3703-4005-8fa9-7065bb35675d)
![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/b2c0209c-64af-4854-b5e5-af499e4dcad8)
![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/2777a6fb-c1a4-4399-9a33-48b44a9b3096)

### Эксперимент с удалением и перемещением файлов (третий и четвёртый коммит)

1. Создайте файлы `will_be_deleted.txt` (с текстом `will_be_deleted`) и `will_be_moved.txt` (с текстом `will_be_moved`) и закоммите их с комментарием `Prepare to delete and move`.
2. 
![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/fd177e34-7a36-4d47-896f-ab0754952dea)
![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/489877c8-98e2-4af9-ad10-22860ebc0b76)
![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/49af6aaf-9fdf-4723-816b-103a0e544a99)

3. В случае необходимости обратитесь к [официальной документации](https://git-scm.com/book/ru/v2/Основы-Git-Запись-изменений-в-репозиторий) — здесь подробно описано, как выполнить следующие шаги.
4. Удалите файл `will_be_deleted.txt` с диска и из репозитория.

![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/719def32-428c-4ecd-833e-e2203a6f9ec2)

5. Переименуйте (переместите) файл `will_be_moved.txt` на диске и в репозитории, чтобы он стал называться `has_been_moved.txt`.

![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/f8f2ff6c-08d0-4559-9e41-dd275ae80e25)
   
6. Закоммитьте результат работы с комментарием `Moved and deleted`.

![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/1148440b-5a2a-4b8f-bc54-a4f7be4b2f06)

### Проверка изменения

1. В результате предыдущих шагов в репозитории должно быть как минимум пять коммитов (если вы сделали ещё промежуточные — нет проблем):
    * `Initial Commit` — созданный GitHub при инициализации репозитория. 
    * `First commit` — созданный после изменения файла `README.md`.
    * `Added gitignore` — после добавления `.gitignore`.
    * `Prepare to delete and move` — после добавления двух временных файлов.
    * `Moved and deleted` — после удаления и перемещения временных файлов. 
2. Проверьте это, используя комманду `git log`. Подробно о формате вывода этой команды мы поговорим на следующем занятии, но посмотреть, что она отображает, можно уже сейчас.

![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/fef4a7e9-4b01-42d8-9faf-7313cbfbe98e)

### Отправка изменений в репозиторий

Выполните команду `git push`, если Git запросит логин и пароль — введите ваши логин и пароль от GitHub. 

В качестве результата отправьте ссылку на репозиторий. 

![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/431eae59-9e35-4cfc-a04f-c1500e40262d)
![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/7d7962e1-0686-49fc-b02a-367acb610f20)

https://github.com/bezymel/devops-netology

----

### Правила приёма домашнего задания

В личном кабинете отправлена ссылка на ваш репозиторий.


### Критерии оценки

Зачёт:

* выполнены все задания;
* ответы даны в развёрнутой форме;
* приложены соответствующие скриншоты и файлы проекта;
* в выполненных заданиях нет противоречий и нарушения логики.

На доработку:

* задание выполнено частично или не выполнено вообще;
* в логике выполнения заданий есть противоречия и существенные недостатки.



