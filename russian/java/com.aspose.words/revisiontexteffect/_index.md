---
title: RevisionTextEffect
second_title: Справочник по API Aspose.Words для Java
description: Позволяет указать эффект оформления для редакций текста документа.
type: docs
weight: 489
url: /ru/java/com.aspose.words/revisiontexteffect/
---

**Наследование:**
java.lang.Object
```
public class RevisionTextEffect
```

Позволяет указать эффект оформления для редакций текста документа.
## Поля

| Поле | Описание |
| --- | --- |
| [BOLD](#BOLD) | Пересмотренное содержимое выделено жирным шрифтом и окрашено. |
| [COLOR](#COLOR) | Измененный контент выделяется только цветом. |
| [DOUBLE_STRIKE_THROUGH](#DOUBLE-STRIKE-THROUGH) | Отредактированный контент зачеркнут двойным штрихом и окрашен. |
| [DOUBLE_UNDERLINE](#DOUBLE-UNDERLINE) | Отредактированное содержимое подчеркнуто двойным подчеркиванием и окрашено. |
| [HIDDEN](#HIDDEN) | Измененный контент скрыт. |
| [ITALIC](#ITALIC) | Исправленное содержание выделено курсивом и окрашено. |
| [NONE](#NONE) | К переработанному контенту не применяются специальные эффекты. |
| [STRIKE_THROUGH](#STRIKE-THROUGH) | Отредактированный контент зачеркнут и окрашен. |
| [UNDERLINE](#UNDERLINE) | Измененное содержимое подчеркнуто и окрашено. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String revisionTextEffectName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int revisionTextEffect)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int revisionTextEffect)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### BOLD {#BOLD}
```
public static int BOLD
```


Пересмотренное содержимое выделено жирным шрифтом и окрашено.

### COLOR {#COLOR}
```
public static int COLOR
```


Измененный контент выделяется только цветом.

### DOUBLE_STRIKE_THROUGH {#DOUBLE-STRIKE-THROUGH}
```
public static int DOUBLE_STRIKE_THROUGH
```


 Отредактированный контент зачеркнут двойным штрихом и окрашен. Работает только для[RevisionType.DELETION](../../com.aspose.words/revisiontype\#DELETION), [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype\#FORMAT-CHANGE) а также[RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING) (тип «перейти от»).

### DOUBLE_UNDERLINE {#DOUBLE-UNDERLINE}
```
public static int DOUBLE_UNDERLINE
```


Отредактированное содержимое подчеркнуто двойным подчеркиванием и окрашено.

### HIDDEN {#HIDDEN}
```
public static int HIDDEN
```


Измененный контент скрыт. Работает только для[RevisionType.DELETION](../../com.aspose.words/revisiontype\#DELETION) а также[RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING) (тип «перейти от»).

### ITALIC {#ITALIC}
```
public static int ITALIC
```


Исправленное содержание выделено курсивом и окрашено.

### NONE {#NONE}
```
public static int NONE
```


 К переработанному контенту не применяются специальные эффекты. Это соответствует[RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor\#NO-HIGHLIGHT).

### STRIKE_THROUGH {#STRIKE-THROUGH}
```
public static int STRIKE_THROUGH
```


Отредактированный контент зачеркнут и окрашен.

### UNDERLINE {#UNDERLINE}
```
public static int UNDERLINE
```


Измененное содержимое подчеркнуто и окрашено.

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
### fromName(String revisionTextEffectName) {#fromName-java.lang.String-}
```
public static int fromName(String revisionTextEffectName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| revisionTextEffectName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int revisionTextEffect) {#getName-int-}
```
public static String getName(int revisionTextEffect)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| revisionTextEffect | int |  |

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
### toString(int revisionTextEffect) {#toString-int-}
```
public static String toString(int revisionTextEffect)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| revisionTextEffect | int |  |

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
