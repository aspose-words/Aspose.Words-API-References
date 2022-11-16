---
title: ReplacingArgs
second_title: Справочник по API Aspose.Words для Java
description: Предоставляет данные для пользовательской операции замены.
type: docs
weight: 476
url: /ru/java/com.aspose.words/replacingargs/
---

**Наследование:**
java.lang.Object
```
public class ReplacingArgs
```

Предоставляет данные для пользовательской операции замены.

 Чтобы узнать больше, посетите**Find and Replace** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getGroupIndex()](#getGroupIndex--) |  Идентифицирует по индексу захваченную группу в[getMatch()](../../com.aspose.words/replacingargs\#getMatch--) который подлежит замене на[getReplacement()](../../com.aspose.words/replacingargs\#getReplacement--) / [setReplacement(java.lang.String)](../../com.aspose.words/replacingargs\#setReplacement-java.lang.String-) нить. |
| [getMatch()](#getMatch--) |  java.util.regex.Matcher, полученный в результате совпадения одного регулярного выражения во время**Replace**. |
| [getMatchNode()](#getMatchNode--) | Получает узел, содержащий начало совпадения. |
| [getMatchOffset()](#getMatchOffset--) | Получает отсчитываемую от нуля начальную позицию совпадения от начала узла, содержащего начало совпадения. |
| [getReplacement()](#getReplacement--) | Получает строку замены. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setGroupIndex(int value)](#setGroupIndex-int-) |  Идентифицирует по индексу захваченную группу в[getMatch()](../../com.aspose.words/replacingargs\#getMatch--) который подлежит замене на[getReplacement()](../../com.aspose.words/replacingargs\#getReplacement--) / [setReplacement(java.lang.String)](../../com.aspose.words/replacingargs\#setReplacement-java.lang.String-) нить. |
| [setReplacement(String value)](#setReplacement-java.lang.String-) | Устанавливает строку замены. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getGroupIndex() {#getGroupIndex--}
```
public int getGroupIndex()
```


 Идентифицирует по индексу захваченную группу в[getMatch()](../../com.aspose.words/replacingargs\#getMatch--) который подлежит замене на[getReplacement()](../../com.aspose.words/replacingargs\#getReplacement--) / [setReplacement(java.lang.String)](../../com.aspose.words/replacingargs\#setReplacement-java.lang.String-) нить.

По умолчанию ноль.

**Возвращает:**
int - соответствующее значение int.
### getMatch() {#getMatch--}
```
public Matcher getMatch()
```


 java.util.regex.Matcher, полученный в результате совпадения одного регулярного выражения во время**Replace**.

Matcher.start() получает начальную позицию совпадения, отсчитываемую от нуля, с начала диапазона поиска и замены.

**Возвращает:**
java.util.regex.Matcher — соответствующее значение java.util.regex.Matcher.
### getMatchNode() {#getMatchNode--}
```
public Node getMatchNode()
```


Получает узел, содержащий начало совпадения.

**Возвращает:**
[Node](../../com.aspose.words/node) - Узел, содержащий начало совпадения.
### getMatchOffset() {#getMatchOffset--}
```
public int getMatchOffset()
```


Получает отсчитываемую от нуля начальную позицию совпадения от начала узла, содержащего начало совпадения.

**Возвращает:**
int — начальная позиция совпадения, отсчитываемая от нуля, от начала узла, содержащего начало совпадения.
### getReplacement() {#getReplacement--}
```
public String getReplacement()
```


Получает строку замены.

**Возвращает:**
java.lang.String — строка замены.
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




### setGroupIndex(int value) {#setGroupIndex-int-}
```
public void setGroupIndex(int value)
```


 Идентифицирует по индексу захваченную группу в[getMatch()](../../com.aspose.words/replacingargs\#getMatch--) который подлежит замене на[getReplacement()](../../com.aspose.words/replacingargs\#getReplacement--) / [setReplacement(java.lang.String)](../../com.aspose.words/replacingargs\#setReplacement-java.lang.String-) нить.

По умолчанию ноль.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее целочисленное значение. |

### setReplacement(String value) {#setReplacement-java.lang.String-}
```
public void setReplacement(String value)
```


Устанавливает строку замены.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Строка замены. |

### toString() {#toString--}
```
public String toString()
```




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
