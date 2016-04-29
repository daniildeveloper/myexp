# Что такое модуль?

  Netbeans - модульное приложение. Это значит, что оно состоит из частей, которые открываются во время выполнения программы. Некоторые из этих частей могут быть скачанны и установленны или удаленны пока программа работает.
  
  Модуль - это библиотека. Это Java JAR (Java Архив) содержащий некоторые классы.
  
  NetBeans - приложение, написанное на Java. У приложения очень маленькое ядро, которое знает как найти модули из которых состоит приложение(программа запуска/launcher проходит по списку директорий/папок - так называемых кластеров - которые содержат JAR файлы и XML-метаданные о них).
  
  Весь функционал Netbeans IDE или любых других приложений, основанных на ядре Netbeans реализуется в виде модулей.
  
  Каждый модуль JAR содержит некоторые дополнительные записи в файле META-INF/MANIFEST.MF, который указывает NetBeans имя модуля, версию модуля и т. д.
  
  Одно отличие модулей NetBeans от JAR заключается в том, чтобы вызвать код в другом модуле, отличном от вашего, вам нужно объявить зависимость в другом модуле. ???
  
  
  
### Английский вариант:


  NetBeans is a modular application. That means it is composed of pieces, which are discovered at runtime. Some of those pieces may even be downloaded and installed or uninstalled at runtime.

A module is a library. It is a Java JAR (Java ARchive) file which contains some classes.

NetBeans is a Java application. It has a very small core runtime which knows how to find the modules that make up the application (the launcher passes a list of directories - these are commonly called clusters - which contain module JAR files and some XML metadata about them).

All real functionality of the NetBeans IDE or any NetBeans-based application is implemented as modules.

A module JAR contains some additional entries in its META-INF/MANIFEST.MF file, which tell NetBeans about the module - its name, its version, etc.

One distinction about NetBeans modules, as opposed to just working with JAR files on your classpath is that the NetBeans runtime enforces dependency management between modules - to call code in another module from yours, your module must declare a dependency on the other module.

Another significant distinction is that a module can specify which (if any) packages it makes visible to modules that depend on it - so it is possible to have Java packages in a module's JAR file which are visible only to other classes within that JAR file. That, in effect, extends Java's class visibility-scoping rules (public, protected, private, package-private) to include public only within this JAR file.
  