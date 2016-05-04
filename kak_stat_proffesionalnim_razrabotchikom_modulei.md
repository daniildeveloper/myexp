# Как стать проффесиональным разработчиком модулей

У NetBeans своя кривая обучения. Цель данного FAQ - быстрый старт. Чтобы быть проффесионалом, не обязательно знять все, что только можно знать. Это значит, что вы можете находить то, что вам нужно, только тогда, когда это действительно необходимо. И здесь некоторые моменты.

  
### Javadoc
  Всю необходимую документацию по NetBeans API можно найти [здесь](http://bits.netbeans.org/dev/javadoc/index.html).
  
  Если вам нужна локальная копия, вы можете скачать ее из центра обновлений или собрать из исходников следующим скриптом:
  ```
    $ cd NB_SRC_ROOT
    $ ant buil-javadoc
  ```
 
### Использование Javadoc
 Список всех API находится в верхней левой части документации. Ограничивается просто классами к конкретному API. 
 

###  NetBeans Tutorials
 [Здесь](https://netbeans.org/kb/trails/platform.html) список всех обучалок по NetBeans.
 
 
### Работа с исходным кодом
 Некоторые люди утверждают, что им никогда не нужно смотреть в исходный код программы, мол де документации хватает за глаза. Это глупо. Код NetBeans - кладезь того как делать те или иные вещи.
 
 С 2008 года все исходники NetBeans находятся в репозитории  Mercurial [здесь](hg.netbeans.org).
 
 Вы также можете посмотреть всю документацию по Mercurial [здесь](http://deadlock.netbeans.org/hudson/job/faqsuck/lastSuccessfulBuild/artifact/other/faqsuck/build/faq.html#HgMigrationDocs). Если вы уже знакомы c Mercurial, можете сразу отправляться в [HhHowTos](http://deadlock.netbeans.org/hudson/job/faqsuck/lastSuccessfulBuild/artifact/other/faqsuck/build/faq.html#HgHowTos). 
 
 Вы увидите множество самых лучших NetBeans проектов. Большинство из них открывается как проекты в  NetBeans.
 
 [Здесь](http://deadlock.netbeans.org/hudson/job/faqsuck/lastSuccessfulBuild/artifact/other/faqsuck/build/faq.html#HgHowTos#Doing_your_first_build) то, как все это собрать.
 
 Сборка Netbeans создаст ```nbbuild/netbeans```.
 
 
 ### Как создать используемое API
 
 
 
 