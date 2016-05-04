# Window System Api

| package | Описание |
| -- | -- |
| org.openide.windows | Большинство частей не работают с окнами напрямую, но используют специальные инструменты |

##Случаи использования
Для более подробного ознакомления с концепцией прочти 6-ю главу книги "Netbeans Platform for Beginners" by Jason Wexbridge and Walter Nyland.

###основные случаи использования
Основны случаи использования можно прочесть в специальном документе.

###Как создать файл ".settings" для TopComponent
Either write it by hand (not that hard if you copy other file and tweak it to match your TC), or start the IDE, instantiate the TC somehow (You have a "Window->Show My TC", right? ), copy the file that gets created in $userdir/config/Windows2Local/Component and cleanup the serialdata section - replace it with proper 
```
"<instance class='..." />
```
 tag.
