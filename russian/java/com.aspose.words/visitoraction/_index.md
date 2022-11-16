---
title: VisitorAction
second_title: Справочник по API Aspose.Words для Java
description: Позволяет посетителю контролировать перечисление узлов.
type: docs
weight: 603
url: /ru/java/com.aspose.words/visitoraction/
---

**Наследование:**
java.lang.Object
```
public class VisitorAction
```

Позволяет посетителю контролировать перечисление узлов.
## Поля

| Поле | Описание |
| --- | --- |
| [CONTINUE](#CONTINUE) | Посетитель просит продолжить перечисление. |
| [SKIP_THIS_NODE](#SKIP-THIS-NODE) | Посетитель просит пропустить текущий узел и продолжить перечисление. |
| [STOP](#STOP) | Посетитель запрашивает остановку перечисления узлов. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String visitorActionName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int visitorAction)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int visitorAction)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### CONTINUE {#CONTINUE}
```
public static int CONTINUE
```


Посетитель просит продолжить перечисление.

### SKIP_THIS_NODE {#SKIP-THIS-NODE}
```
public static int SKIP_THIS_NODE
```


Посетитель просит пропустить текущий узел и продолжить перечисление.

### STOP {#STOP}
```
public static int STOP
```


Посетитель запрашивает остановку перечисления узлов.

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
### fromName(String visitorActionName) {#fromName-java.lang.String-}
```
public static int fromName(String visitorActionName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| visitorActionName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int visitorAction) {#getName-int-}
```
public static String getName(int visitorAction)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| visitorAction | int |  |

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
### toString(int visitorAction) {#toString-int-}
```
public static String toString(int visitorAction)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| visitorAction | int |  |

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
