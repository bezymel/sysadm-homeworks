# Домашнее задание к занятию «Инструменты Git»

### Цель задания

В результате выполнения задания вы:

* научитесь работать с утилитами Git;
* потренируетесь решать типовые задачи, возникающие при работе в команде. 

### Инструкция к заданию

1. Склонируйте [репозиторий](https://github.com/hashicorp/terraform) с исходным кодом Terraform.

![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/aaa43393-fbc5-4a81-af36-27191868b65b)

2. Создайте файл для ответов на задания в своём репозитории, после выполнения прикрепите ссылку на .md-файл с ответами в личном кабинете.

![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/500f466d-e1d4-4818-8c54-ff929bbee65a)

4. Любые вопросы по решению задач задавайте в чате учебной группы.

------

## Задание

В клонированном репозитории:

1. Найдите полный хеш и комментарий коммита, хеш которого начинается на `aefea`.

![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/6afd2f51-03c0-41ba-a065-967b0c2cb313)

git show aefea

Полный хэш: aefead2207ef7e2aa5dc81a34aedf0cad4c32545

Комментарий: Update CHANGELOG.md

2. Ответьте на вопросы.


1. Какому тегу соответствует коммит `85024d3`?

![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/605d912b-9879-4c62-8434-a6b31479f305)

git show 85024d3

commit 85024d3100126de36331c6982bfaac02cdab9e76 (tag: v0.12.23)

Тег: v0.12.23

2. Сколько родителей у коммита `b8d720`? Напишите их хеши.

![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/be39350f-4ed8-46bb-b55c-4c3a4601634d)

Два родителя:

56cd7859e0 

9ea88f22fc

3. Перечислите хеши и комментарии всех коммитов, которые были сделаны между тегами  v0.12.23 и v0.12.24.

git log v0.12.23..v0.12.24

![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/8107f919-6ac9-4fd2-8828-115d7f7b2e79)
![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/5664612d-a20d-45d8-ab6a-c59b0ddb1461)

- commit 33ff1c03bb960b332be3af2e333462dde88b279e (tag: v0.12.24)
  v0.12.24
  
- commit b14b74c4939dcab573326f4e3ee2a62e23e12f89
  [Website] vmc provider links
  
- commit 3f235065b9347a758efadc92295b540ee0a5e26e
  Update CHANGELOG.md
  
- commit 6ae64e247b332925b872447e9ce869657281c2bf
  registry: Fix panic when server is unreachable
  Non-HTTP errors previously resulted in a panic due to dereferencing the resp pointer while it was nil, as part of rendering the error message. This * commit changes the error message formatting to cope 
  with a nil response, and extends test coverage.
  Fixes #24384
  
- commit 5c619ca1baf2e21a155fcdb4c264cc9e24a2a353
  *website: Remove links to the getting started guide's old location
  Since these links were in the soon-to-be-deprecated 0.11 language section, I think we can just remove them without needing to find an equivalent link.
  
- commit 06275647e2b53d97d4f0a19a0fec11f6d69820b5
  Update CHANGELOG.md
  
- commit d5f9411f5108260320064349b757f55c09bc4b80
  command: Fix bug when using terraform login on Windows
  
- commit 4b6d06cc5dcb78af637bbb19c198faff37a066ed
  Update CHANGELOG.md
  
- commit dd01a35078f040ca984cdd349f18d0b67e486c35
  Update CHANGELOG.md
  
- commit 225466bc3e5f35baa5d07197bbc079345b77525e
  Cleanup after v0.12.23 release

4. Найдите коммит, в котором была создана функция `func providerSource`, её определение в коде выглядит так: `func providerSource(...)` (вместо троеточия перечислены аргументы).

git log -S 'func providerSource'

![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/87d6506c-e4e1-46a5-b315-af4cbdc71feb)

Получили:

- commit 5af1e6234ab6da412fb8637393c5a17a1b293663
  Date:   Tue Apr 21 16:28:59 2020 -0700
  
- commit 8c928e83589d90a031f811fae52a81be7153e82f
  Date:   Thu Apr 2 18:04:39 2020 -0700

Посмотрим более ранний из них:
![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/ad090cab-1aed-48a0-8d6d-59e8906edf92)

git show 8c928e8 | grep "func providerSource"

+func providerSource(services *disco.Disco) getproviders.Source {

Нашли - это коммит 8c928e83589d90a031f811fae52a81be7153e82f

5. Найдите все коммиты, в которых была изменена функция `globalPluginDirs`.
![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/b721e2ef-6b08-4eb1-b57a-62af945a19ed)
![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/21e156de-597b-447d-bd62-87955ee06e69)

git log -S 'globalPluginDirs'

Получили 3 коммита: 

- commit 35a058fb3ddfae9cfee0b3893822c9a95b920f4c
  Date:   Thu Oct 19 17:40:20 2017 -0700
  
- commit c0b17610965450a89598da491ce9b6b5cbd6393f
  Date:   Mon Jun 12 15:04:40 2017 -0400
  
- commit 8364383c359a6b738a436d1b7745ccdce178df47
  Date:   Thu Apr 13 18:05:58 2017 -0700

Соответственно, в наиболее раннем из них функция создана, а в следующих отредактирована:

* c0b17610965450a89598da491ce9b6b5cbd6393f
* 35a058fb3ddfae9cfee0b3893822c9a95b920f4c

6. Кто автор функции `synchronizedWriters`?
![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/83e1d5be-5917-4e16-aed2-bdadb6830fdf)

git log -S "synchronizedWriters"
Наиболее ранний коммит:

 - commit 5ac311e2a91e381e2f52234668b49ba670aa0fe5
   Author: Martin Atkins mart@degeneration.co.uk
   
Посмотрим, в каких файлах эта функция упоминается: git grep --break -n "synchronizedWriters" 5ac311e2a91e381e2f52234668b49ba670aa0fe5
![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/0ef14444-998e-4297-b6c1-4130ff609456)
![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/5459f63e-0600-4fe7-a934-1c703cecc6d1)
![image](https://github.com/bezymel/sysadm-homeworks/assets/129361495/dab1f518-caae-4bd0-ac55-95064a70cddd)
Автор: Martin Atkins


*В качестве решения ответьте на вопросы и опишите, как были получены эти ответы.*

---

### Правила приёма домашнего задания

В личном кабинете отправлена ссылка на .md-файл в вашем репозитории.

### Критерии оценки

Зачёт:

* выполнены все задания;
* ответы даны в развёрнутой форме;
* приложены соответствующие скриншоты и файлы проекта;
* в выполненных заданиях нет противоречий и нарушения логики.

На доработку:

* задание выполнено частично или не выполнено вообще;
* в логике выполнения заданий есть противоречия и существенные недостатки.
