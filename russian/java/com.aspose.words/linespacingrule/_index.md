---
title: LineSpacingRule
second_title: Справочник по API Aspose.Words для Java
description: Указывает значения межстрочного интервала для абзаца.
type: docs
weight: 366
url: /ru/java/com.aspose.words/linespacingrule/
---

**Наследование:**
java.lang.Object
```
public class LineSpacingRule
```

Указывает значения межстрочного интервала для абзаца.
## Поля

| Поле | Описание |
| --- | --- |
| [AT_LEAST](#AT-LEAST) |  Межстрочный интервал может быть больше или равен, но не меньше значения, указанного в[ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat\#getLineSpacing--) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat\#setLineSpacing-double-) имущество. |
| [EXACTLY](#EXACTLY) |  Межстрочный интервал никогда не меняется от значения, указанного в[ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat\#getLineSpacing--) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat\#setLineSpacing-double-) свойство, даже если в абзаце используется более крупный шрифт. |
| [MULTIPLE](#MULTIPLE) |  Межстрочный интервал указан в[ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat\#getLineSpacing--) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat\#setLineSpacing-double-) свойство как количество строк. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String lineSpacingRuleName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int lineSpacingRule)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int lineSpacingRule)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### AT_LEAST {#AT-LEAST}
```
public static int AT_LEAST
```


 Межстрочный интервал может быть больше или равен, но не меньше значения, указанного в[ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat\#getLineSpacing--) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat\#setLineSpacing-double-) имущество.

### EXACTLY {#EXACTLY}
```
public static int EXACTLY
```


 Межстрочный интервал никогда не меняется от значения, указанного в[ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat\#getLineSpacing--) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat\#setLineSpacing-double-) свойство, даже если в абзаце используется более крупный шрифт.

### MULTIPLE {#MULTIPLE}
```
public static int MULTIPLE
```


 Межстрочный интервал указан в[ParagraphFormat.getLineSpacing()](../../com.aspose.words/paragraphformat\#getLineSpacing--) / [ParagraphFormat.setLineSpacing(double)](../../com.aspose.words/paragraphformat\#setLineSpacing-double-) свойство как количество строк. Одна линия равна 12 очкам.

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
### fromName(String lineSpacingRuleName) {#fromName-java.lang.String-}
```
public static int fromName(String lineSpacingRuleName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| lineSpacingRuleName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int lineSpacingRule) {#getName-int-}
```
public static String getName(int lineSpacingRule)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| lineSpacingRule | int |  |

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
### toString(int lineSpacingRule) {#toString-int-}
```
public static String toString(int lineSpacingRule)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| lineSpacingRule | int |  |

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
