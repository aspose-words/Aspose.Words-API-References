---
title: FontFamily
second_title: Справочник по API Aspose.Words для Java
description: Представляет семейство шрифтов.
type: docs
weight: 278
url: /ru/java/com.aspose.words/fontfamily/
---

**Наследование:**
java.lang.Object
```
public class FontFamily
```

Представляет семейство шрифтов.

Семейство шрифтов — это набор шрифтов, имеющих общие характеристики ширины штриха и засечек.
## Поля

| Поле | Описание |
| --- | --- |
| [AUTO](#AUTO) | Указывает общее имя семейства. |
| [DECORATIVE](#DECORATIVE) | Задает новый шрифт. |
| [MODERN](#MODERN) | Определяет моноширинный шрифт с засечками или без них. |
| [ROMAN](#ROMAN) | Определяет пропорциональный шрифт с засечками. |
| [SCRIPT](#SCRIPT) | Определяет шрифт, который должен выглядеть как рукописный; примеры включают Script и Cursive. |
| [SWISS](#SWISS) | Определяет пропорциональный шрифт без засечек. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String fontFamilyName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int fontFamily)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int fontFamily)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Указывает общее имя семейства. Это имя используется, когда информация о шрифте не существует или не имеет значения. Используется шрифт по умолчанию.

### DECORATIVE {#DECORATIVE}
```
public static int DECORATIVE
```


Задает новый шрифт. Например, древнеанглийский.

### MODERN {#MODERN}
```
public static int MODERN
```


Определяет моноширинный шрифт с засечками или без них. Моноширинные шрифты обычно современные; примеры включают Pica, Elite и Courier New.

### ROMAN {#ROMAN}
```
public static int ROMAN
```


Определяет пропорциональный шрифт с засечками. Например, Times New Roman.

### SCRIPT {#SCRIPT}
```
public static int SCRIPT
```


Определяет шрифт, который должен выглядеть как рукописный; примеры включают Script и Cursive.

### SWISS {#SWISS}
```
public static int SWISS
```


Определяет пропорциональный шрифт без засечек. Пример - Ариал.

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
### fromName(String fontFamilyName) {#fromName-java.lang.String-}
```
public static int fromName(String fontFamilyName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fontFamilyName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int fontFamily) {#getName-int-}
```
public static String getName(int fontFamily)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fontFamily | int |  |

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
### toString(int fontFamily) {#toString-int-}
```
public static String toString(int fontFamily)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fontFamily | int |  |

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
