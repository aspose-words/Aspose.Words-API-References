---
title: ContinuousSectionRestart
second_title: Справочник по API Aspose.Words для Java
description: Представляет различное поведение при вычислении номеров страниц в непрерывном разделе, который перезапускает нумерацию страниц.
type: docs
weight: 93
url: /ru/java/com.aspose.words/continuoussectionrestart/
---

**Наследование:**
java.lang.Object
```
public class ContinuousSectionRestart
```

Представляет различное поведение при вычислении номеров страниц в непрерывном разделе, который перезапускает нумерацию страниц.
## Поля

| Поле | Описание |
| --- | --- |
| [ALWAYS](#ALWAYS) | Нумерация страниц всегда перезапускается независимо от потока содержимого. |
| [FROM_NEW_PAGE_ONLY](#FROM-NEW-PAGE-ONLY) | Нумерация страниц возобновляется только в том случае, если перед разделом на странице, с которой начинается раздел, нет другого содержимого. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String continuousSectionRestartName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int continuousSectionRestart)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int continuousSectionRestart)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### ALWAYS {#ALWAYS}
```
public static int ALWAYS
```


Нумерация страниц всегда перезапускается независимо от потока содержимого. Такое поведение демонстрируют все версии MS Word, кроме Word 2016.

### FROM_NEW_PAGE_ONLY {#FROM-NEW-PAGE-ONLY}
```
public static int FROM_NEW_PAGE_ONLY
```


Нумерация страниц возобновляется только в том случае, если перед разделом на странице, с которой начинается раздел, нет другого содержимого. Поведение демонстрирует MS Word 2016.

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
### fromName(String continuousSectionRestartName) {#fromName-java.lang.String-}
```
public static int fromName(String continuousSectionRestartName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| continuousSectionRestartName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int continuousSectionRestart) {#getName-int-}
```
public static String getName(int continuousSectionRestart)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| continuousSectionRestart | int |  |

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
### toString(int continuousSectionRestart) {#toString-int-}
```
public static String toString(int continuousSectionRestart)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| continuousSectionRestart | int |  |

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
