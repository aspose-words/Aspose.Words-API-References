---
title: HtmlVersion
second_title: Справочник по API Aspose.Words для Java
description: Указывает версию HTML, используемую при сохранении документа в форматы и .
type: docs
weight: 332
url: /ru/java/com.aspose.words/htmlversion/
---

**Наследование:**
java.lang.Object
```
public class HtmlVersion
```

 Указывает версию HTML, используемую при сохранении документа в[SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML) а также[SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML) форматы.
## Поля

| Поле | Описание |
| --- | --- |
| [HTML_5](#HTML-5) | Сохраняет документ в соответствии со стандартом HTML 5. |
| [XHTML](#XHTML) | Сохраняет документ в соответствии со стандартом XHTML 1.0 Transitional. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String htmlVersionName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int htmlVersion)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int htmlVersion)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### HTML_5 {#HTML-5}
```
public static int HTML_5
```


Сохраняет документ в соответствии со стандартом HTML 5.

### XHTML {#XHTML}
```
public static int XHTML
```


Сохраняет документ в соответствии со стандартом XHTML 1.0 Transitional.

Aspose.Words стремится выводить XHTML в соответствии со стандартом XHTML 1.0 Transitional, но вывод не всегда будет проверяться на соответствие DTD. Некоторые структуры внутри документа Microsoft Word трудно или невозможно сопоставить с документом, который будет проверяться на соответствие схеме XHTML. Например, XHTML не допускает вложенных списков (UL не может быть вложен в другой элемент UL), но в документах Microsoft Word довольно часто встречаются многоуровневые списки.

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
### fromName(String htmlVersionName) {#fromName-java.lang.String-}
```
public static int fromName(String htmlVersionName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| htmlVersionName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int htmlVersion) {#getName-int-}
```
public static String getName(int htmlVersion)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| htmlVersion | int |  |

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
### toString(int htmlVersion) {#toString-int-}
```
public static String toString(int htmlVersion)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| htmlVersion | int |  |

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
