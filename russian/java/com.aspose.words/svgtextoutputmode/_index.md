---
title: SvgTextOutputMode
second_title: Справочник по API Aspose.Words для Java
description: 
type: docs
weight: 542
url: /ru/java/com.aspose.words/svgtextoutputmode/
---

**Наследование:**
java.lang.Object
```
public class SvgTextOutputMode
```
## Поля

| Поле | Описание |
| --- | --- |
| [USE_PLACED_GLYPHS](#USE-PLACED-GLYPHS) | Текст визуализируется с помощью кривых. |
| [USE_SVG_FONTS](#USE-SVG-FONTS) | Шрифты SVG используются для отображения текста. |
| [USE_TARGET_MACHINE_FONTS](#USE-TARGET-MACHINE-FONTS) | Шрифты, установленные на целевой машине, используются для отображения текста. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String svgTextOutputModeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int svgTextOutputMode)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int svgTextOutputMode)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### USE_PLACED_GLYPHS {#USE-PLACED-GLYPHS}
```
public static int USE_PLACED_GLYPHS
```


Текст визуализируется с помощью кривых. Обратите внимание, что выделение текста не будет работать, если вы используете эту опцию.

### USE_SVG_FONTS {#USE-SVG-FONTS}
```
public static int USE_SVG_FONTS
```


Шрифты SVG используются для отображения текста. Обратите внимание, что не все браузеры поддерживают шрифты SVG.

### USE_TARGET_MACHINE_FONTS {#USE-TARGET-MACHINE-FONTS}
```
public static int USE_TARGET_MACHINE_FONTS
```


Шрифты, установленные на целевой машине, используются для отображения текста. Обратите внимание: если некоторые шрифты, используемые в документе, недоступны на целевой машине, документ может выглядеть иначе.

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
### fromName(String svgTextOutputModeName) {#fromName-java.lang.String-}
```
public static int fromName(String svgTextOutputModeName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| svgTextOutputModeName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int svgTextOutputMode) {#getName-int-}
```
public static String getName(int svgTextOutputMode)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| svgTextOutputMode | int |  |

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
### toString(int svgTextOutputMode) {#toString-int-}
```
public static String toString(int svgTextOutputMode)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| svgTextOutputMode | int |  |

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
