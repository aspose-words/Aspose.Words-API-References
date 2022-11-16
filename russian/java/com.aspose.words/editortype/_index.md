---
title: EditorType
second_title: Справочник по API Aspose.Words для Java
description: Задает набор возможных псевдонимов или групп редактирования, которые можно использовать в качестве псевдонимов, чтобы определить, разрешено ли текущему пользователю редактировать один диапазон, определенный редактируемым диапазоном в документе.
type: docs
weight: 140
url: /ru/java/com.aspose.words/editortype/
---

**Наследование:**
java.lang.Object
```
public class EditorType
```

Задает набор возможных псевдонимов (или групп редактирования), которые можно использовать в качестве псевдонимов, чтобы определить, разрешено ли текущему пользователю редактировать один диапазон, определенный редактируемым диапазоном в документе.
## Поля

| Поле | Описание |
| --- | --- |
| [ADMINISTRATORS](#ADMINISTRATORS) | Указывает, что пользователям, связанным с группой «Администраторы», должно быть разрешено редактировать редактируемые диапазоны с использованием этого типа редактирования, когда включена защита документа. |
| [CONTRIBUTORS](#CONTRIBUTORS) | Указывает, что пользователям, связанным с группой Contributors, должно быть разрешено редактировать редактируемые диапазоны, используя этот тип редактирования, когда включена защита документа. |
| [CURRENT](#CURRENT) | Указывает, что пользователям, связанным с текущей группой, должно быть разрешено редактировать редактируемые диапазоны, используя этот тип редактирования, когда включена защита документа. |
| [DEFAULT](#DEFAULT) |  Такой же как[UNSPECIFIED](../../com.aspose.words/editortype\#UNSPECIFIED). |
| [EDITORS](#EDITORS) | Указывает, что пользователям, связанным с группой «Редакторы», должно быть разрешено редактировать редактируемые диапазоны, используя этот тип редактирования, когда включена защита документа. |
| [EVERYONE](#EVERYONE) | Указывает, что всем пользователям, открывающим документ, должно быть разрешено редактировать редактируемые диапазоны, используя этот тип редактирования, когда включена защита документа. |
| [NONE](#NONE) | Указывает, что ни один из пользователей, открывающих документ, не может редактировать редактируемые диапазоны, используя этот тип редактирования, когда включена защита документа. |
| [OWNERS](#OWNERS) | Указывает, что пользователям, связанным с группой «Владельцы», должно быть разрешено редактировать редактируемые диапазоны с использованием этого типа редактирования, когда включена защита документа. |
| [UNSPECIFIED](#UNSPECIFIED) | Означает, что тип редактора не указан. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String editorTypeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int editorType)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int editorType)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### ADMINISTRATORS {#ADMINISTRATORS}
```
public static int ADMINISTRATORS
```


Указывает, что пользователям, связанным с группой «Администраторы», должно быть разрешено редактировать редактируемые диапазоны с использованием этого типа редактирования, когда включена защита документа.

### CONTRIBUTORS {#CONTRIBUTORS}
```
public static int CONTRIBUTORS
```


Указывает, что пользователям, связанным с группой Contributors, должно быть разрешено редактировать редактируемые диапазоны, используя этот тип редактирования, когда включена защита документа.

### CURRENT {#CURRENT}
```
public static int CURRENT
```


Указывает, что пользователям, связанным с текущей группой, должно быть разрешено редактировать редактируемые диапазоны, используя этот тип редактирования, когда включена защита документа.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


 Такой же как[UNSPECIFIED](../../com.aspose.words/editortype\#UNSPECIFIED).

### EDITORS {#EDITORS}
```
public static int EDITORS
```


Указывает, что пользователям, связанным с группой «Редакторы», должно быть разрешено редактировать редактируемые диапазоны, используя этот тип редактирования, когда включена защита документа.

### EVERYONE {#EVERYONE}
```
public static int EVERYONE
```


Указывает, что всем пользователям, открывающим документ, должно быть разрешено редактировать редактируемые диапазоны, используя этот тип редактирования, когда включена защита документа.

### NONE {#NONE}
```
public static int NONE
```


Указывает, что ни один из пользователей, открывающих документ, не может редактировать редактируемые диапазоны, используя этот тип редактирования, когда включена защита документа.

### OWNERS {#OWNERS}
```
public static int OWNERS
```


Указывает, что пользователям, связанным с группой «Владельцы», должно быть разрешено редактировать редактируемые диапазоны с использованием этого типа редактирования, когда включена защита документа.

### UNSPECIFIED {#UNSPECIFIED}
```
public static int UNSPECIFIED
```


Означает, что тип редактора не указан.

### length {#length}
```
public static int length
```


### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Возвращает:**
логический
### fromName(String editorTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String editorTypeName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| editorTypeName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int editorType) {#getName-int-}
```
public static String getName(int editorType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| editorType | int |  |

**Возвращает:**
java.lang.String
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Возвращает:**
инт[]
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### toString() {#toString--}
```
public String toString()
```




**Возвращает:**
java.lang.String
### toString(int editorType) {#toString-int-}
```
public static String toString(int editorType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| editorType | int |  |

**Возвращает:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
