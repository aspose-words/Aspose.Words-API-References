---
title: ContentDisposition
second_title: Справочник по API Aspose.Words для Java
description: Перечисляет различные способы представления документа в браузере клиента.
type: docs
weight: 92
url: /ru/java/com.aspose.words/contentdisposition/
---

**Наследование:**
java.lang.Object
```
public class ContentDisposition
```

Перечисляет различные способы представления документа в браузере клиента.

Обратите внимание, что на фактическое поведение в браузере клиента может повлиять конфигурация безопасности браузера.
## Поля

| Поле | Описание |
| --- | --- |
| [ATTACHMENT](#ATTACHMENT) | Отправьте документ в браузер и предоставьте возможность сохранить документ на диск или открыть в приложении, связанном с расширением документа. |
| [INLINE](#INLINE) | Отправьте документ в браузер и предложите сохранить документ на диск или открыть в браузере. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String contentDispositionName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int contentDisposition)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int contentDisposition)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### ATTACHMENT {#ATTACHMENT}
```
public static int ATTACHMENT
```


Отправьте документ в браузер и предоставьте возможность сохранить документ на диск или открыть в приложении, связанном с расширением документа.

### INLINE {#INLINE}
```
public static int INLINE
```


Отправьте документ в браузер и предложите сохранить документ на диск или открыть в браузере.

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
### fromName(String contentDispositionName) {#fromName-java.lang.String-}
```
public static int fromName(String contentDispositionName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| contentDispositionName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int contentDisposition) {#getName-int-}
```
public static String getName(int contentDisposition)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| contentDisposition | int |  |

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
### toString(int contentDisposition) {#toString-int-}
```
public static String toString(int contentDisposition)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| contentDisposition | int |  |

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
