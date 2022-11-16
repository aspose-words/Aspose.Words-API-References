---
title: CompressionLevel
second_title: Справочник по API Aspose.Words для Java
description: Уровень сжатия для файлов OOXML.
type: docs
weight: 88
url: /ru/java/com.aspose.words/compressionlevel/
---

**Наследование:**
java.lang.Object
```
public class CompressionLevel
```

Уровень сжатия для файлов OOXML.

(Файлы DOCX и DOTX внутри являются ZIP-архивом, это свойство определяет уровень сжатия архива.

Обратите внимание, что файл FlatOpc не является ZIP-архивом, поэтому это свойство не влияет на файлы FlatOpc.)
## Поля

| Поле | Описание |
| --- | --- |
| [FAST](#FAST) | Быстрый уровень сжатия. |
| [MAXIMUM](#MAXIMUM) | Максимальный уровень сжатия. |
| [NORMAL](#NORMAL) | Нормальный уровень сжатия. |
| [SUPER_FAST](#SUPER-FAST) | Сверхбыстрый уровень сжатия. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String compressionLevelName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int compressionLevel)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int compressionLevel)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### FAST {#FAST}
```
public static int FAST
```


Быстрый уровень сжатия.

### MAXIMUM {#MAXIMUM}
```
public static int MAXIMUM
```


Максимальный уровень сжатия.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Нормальный уровень сжатия. Уровень сжатия по умолчанию, используемый Aspose.Words.

### SUPER_FAST {#SUPER-FAST}
```
public static int SUPER_FAST
```


Сверхбыстрый уровень сжатия. Microsoft Word использует этот уровень сжатия.

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
### fromName(String compressionLevelName) {#fromName-java.lang.String-}
```
public static int fromName(String compressionLevelName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| compressionLevelName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int compressionLevel) {#getName-int-}
```
public static String getName(int compressionLevel)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| compressionLevel | int |  |

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
### toString(int compressionLevel) {#toString-int-}
```
public static String toString(int compressionLevel)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| compressionLevel | int |  |

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
