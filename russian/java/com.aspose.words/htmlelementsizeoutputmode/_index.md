---
title: HtmlElementSizeOutputMode
second_title: Справочник по API Aspose.Words для Java
description: Указывает, как Aspose.Words экспортирует ширину и высоту элементов в HTML, MHTML и EPUB.
type: docs
weight: 324
url: /ru/java/com.aspose.words/htmlelementsizeoutputmode/
---

**Наследование:**
java.lang.Object
```
public class HtmlElementSizeOutputMode
```

Указывает, как Aspose.Words экспортирует ширину и высоту элементов в HTML, MHTML и EPUB.
## Поля

| Поле | Описание |
| --- | --- |
| [ALL](#ALL) | Экспортируются все размеры элементов, как в абсолютных, так и в относительных единицах, указанные в документе. |
| [NONE](#NONE) | Размеры элементов не экспортируются. |
| [RELATIVE_ONLY](#RELATIVE-ONLY) | Размеры элементов экспортируются, только если они указаны в документе в относительных единицах. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String htmlElementSizeOutputModeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int htmlElementSizeOutputMode)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int htmlElementSizeOutputMode)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### ALL {#ALL}
```
public static int ALL
```


Экспортируются все размеры элементов, как в абсолютных, так и в относительных единицах, указанные в документе.

### NONE {#NONE}
```
public static int NONE
```


Размеры элементов не экспортируются. Визуальные агенты будут автоматически строить макет в соответствии с отношениями между элементами.

### RELATIVE_ONLY {#RELATIVE-ONLY}
```
public static int RELATIVE_ONLY
```


Размеры элементов экспортируются, только если они указаны в документе в относительных единицах. Фиксированные размеры не экспортируются в этом режиме. Визуальные агенты будут вычислять недостающие размеры, чтобы сделать макет документа более естественным.

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
### fromName(String htmlElementSizeOutputModeName) {#fromName-java.lang.String-}
```
public static int fromName(String htmlElementSizeOutputModeName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| htmlElementSizeOutputModeName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int htmlElementSizeOutputMode) {#getName-int-}
```
public static String getName(int htmlElementSizeOutputMode)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| htmlElementSizeOutputMode | int |  |

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
### toString(int htmlElementSizeOutputMode) {#toString-int-}
```
public static String toString(int htmlElementSizeOutputMode)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| htmlElementSizeOutputMode | int |  |

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
