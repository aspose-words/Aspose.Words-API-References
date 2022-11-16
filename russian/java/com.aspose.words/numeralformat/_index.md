---
title: NumeralFormat
second_title: Справочник по API Aspose.Words для Java
description: Указывает набор символов, который используется для представления чисел при отображении в фиксированных форматах страниц.
type: docs
weight: 410
url: /ru/java/com.aspose.words/numeralformat/
---

**Наследование:**
java.lang.Object
```
public class NumeralFormat
```

Указывает набор символов, который используется для представления чисел при отображении в фиксированных форматах страниц.
## Поля

| Поле | Описание |
| --- | --- |
| [ARABIC_INDIC](#ARABIC-INDIC) |  Числительные, используемые в арабском языке:\\u0660\\u0661\\u0662\\u0663\\u0664\\u0665\\u0666\\u0667\\u0668\\u0669. |
| [CONTEXT](#CONTEXT) | Набор символов определяется контекстом (локаль и свойство RTL). |
| [EASTERN_ARABIC_INDIC](#EASTERN-ARABIC-INDIC) |  Числительные, используемые в персидском и урду:\\u06f0\\u06f1\\u06f2\\u06f3\\u06f4\\u06f5\\u06f6\\u06f7\\u06f8\\u06f9. |
| [EUROPEAN](#EUROPEAN) | Европейские цифры: 0123456789. |
| [SYSTEM](#SYSTEM) | ЭТА ВАРИАНТ НЕ ПОДДЕРЖИВАЕТСЯ. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String numeralFormatName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int numeralFormat)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int numeralFormat)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### ARABIC_INDIC {#ARABIC-INDIC}
```
public static int ARABIC_INDIC
```


 Числительные, используемые в арабском языке:\\u0660\\u0661\\u0662\\u0663\\u0664\\u0665\\u0666\\u0667\\u0668\\u0669. Диапазон Юникода от U+0660 до u+0669.

### CONTEXT {#CONTEXT}
```
public static int CONTEXT
```


Набор символов определяется контекстом (локаль и свойство RTL).

### EASTERN_ARABIC_INDIC {#EASTERN-ARABIC-INDIC}
```
public static int EASTERN_ARABIC_INDIC
```


 Числительные, используемые в персидском и урду:\\u06f0\\u06f1\\u06f2\\u06f3\\u06f4\\u06f5\\u06f6\\u06f7\\u06f8\\u06f9. Диапазон Юникода от U+06F0 до u+06F9.

### EUROPEAN {#EUROPEAN}
```
public static int EUROPEAN
```


Европейские цифры: 0123456789.

### SYSTEM {#SYSTEM}
```
public static int SYSTEM
```


ЭТА ВАРИАНТ НЕ ПОДДЕРЖИВАЕТСЯ. Набор символов определяется региональными настройками.

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
### fromName(String numeralFormatName) {#fromName-java.lang.String-}
```
public static int fromName(String numeralFormatName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| numeralFormatName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int numeralFormat) {#getName-int-}
```
public static String getName(int numeralFormat)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| numeralFormat | int |  |

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
### toString(int numeralFormat) {#toString-int-}
```
public static String toString(int numeralFormat)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| numeralFormat | int |  |

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
