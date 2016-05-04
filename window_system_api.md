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

###How to make a TopComponentGroup?
Q: I'm trying to make a TopComponentGroup. I've just read http://ui.netbeans.org/docs/ui/ws/ws_spec.html#3.9 I want to make a group that uses the first invocation strategy. That is, I want the group to open/close when I activate a certain subclass of TopComponent. Say, for example, I have a FooTopComponent, and when it's active, I want to open a FooPropertySheetComponent, docked in a mode on the right-hand side. I know I have to:
declare the group in the layer file (Windows2/Groups)
have code for opening the group
have code for closing the group
I think I do #2 in FooTopComponent.componentActivated() and #3 in FooTopComponent.componentDeactivated(). Is that right?
A:Yes it is correct way. You can check simple test module. First you must get TopComponentGroup instance using find method then call TopComponentGroup.open()/close(). Here is the code in your componentDeactivated method:

```
   protected void componentDeactivated ()
   {
       // close window group containing propsheet, but only if we're
       // selecting a different kind of TC in the same mode
       boolean closeGroup = true;
       Mode curMode = WindowManager.getDefault().findMode(this);
       TopComponent selected = curMode.getSelectedTopComponent();
       if (selected != null && selected instanceof FooTopComponent)
           closeGroup = false;
             if (closeGroup)
       {
           TopComponentGroup group = WindowManager.getDefault().findTopComponentGroup(TC_GROUP);
           if (group != null)
           {
               group.close();
           }
       }
   }  
   ```
    