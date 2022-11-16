---
title: SectionLayoutMode
second_title: Справочник по API Aspose.Words для Java
description: Указывает режим макета для раздела, позволяющий определить поведение сетки документа.
type: docs
weight: 511
url: /ru/java/com.aspose.words/sectionlayoutmode/
---

**Наследование:**
java.lang.Object
```
public class SectionLayoutMode
```

Указывает режим макета для раздела, позволяющий определить поведение сетки документа.
## Поля

| Поле | Описание |
| --- | --- |
| [DEFAULT](#DEFAULT) | Указывает, что сетка документа не должна применяться к содержимому соответствующего раздела в документе. |
| [GRID](#GRID) | Указывает, что в соответствующем разделе должен быть добавлен как дополнительный шаг строки, так и шаг символа к каждой строке и символу внутри нее, чтобы поддерживать определенное количество строк на странице и символов в строке. |
| [LINE_GRID](#LINE-GRID) | Указывает, что в соответствующем разделе к каждой строке должен быть добавлен дополнительный шаг строки, чтобы сохранить указанное количество строк на странице. |
| [SNAP_TO_CHARS](#SNAP-TO-CHARS) | Указывает, что в соответствующем разделе должен быть добавлен как дополнительный шаг строки, так и шаг символа к каждой строке и символу внутри нее, чтобы поддерживать определенное количество строк на странице и символов в строке. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String sectionLayoutModeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int sectionLayoutMode)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int sectionLayoutMode)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Указывает, что сетка документа не должна применяться к содержимому соответствующего раздела в документе.

### GRID {#GRID}
```
public static int GRID
```


Указывает, что в соответствующем разделе должен быть добавлен как дополнительный шаг строки, так и шаг символа к каждой строке и символу внутри нее, чтобы поддерживать определенное количество строк на странице и символов в строке. Символы не будут автоматически выравниваться по линиям сетки при наборе текста.

### LINE_GRID {#LINE-GRID}
```
public static int LINE_GRID
```


Указывает, что в соответствующем разделе к каждой строке должен быть добавлен дополнительный шаг строки, чтобы сохранить указанное количество строк на странице.

### SNAP_TO_CHARS {#SNAP-TO-CHARS}
```
public static int SNAP_TO_CHARS
```


Указывает, что в соответствующем разделе должен быть добавлен как дополнительный шаг строки, так и шаг символа к каждой строке и символу внутри нее, чтобы поддерживать определенное количество строк на странице и символов в строке. Символы будут автоматически выравниваться по линиям сетки при наборе текста.

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
### fromName(String sectionLayoutModeName) {#fromName-java.lang.String-}
```
public static int fromName(String sectionLayoutModeName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| sectionLayoutModeName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int sectionLayoutMode) {#getName-int-}
```
public static String getName(int sectionLayoutMode)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| sectionLayoutMode | int |  |

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
### toString(int sectionLayoutMode) {#toString-int-}
```
public static String toString(int sectionLayoutMode)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| sectionLayoutMode | int |  |

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
