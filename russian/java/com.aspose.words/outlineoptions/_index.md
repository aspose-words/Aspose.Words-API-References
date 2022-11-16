---
title: OutlineOptions
second_title: Справочник по API Aspose.Words для Java
description: Позволяет указать параметры контура.
type: docs
weight: 431
url: /ru/java/com.aspose.words/outlineoptions/
---

**Наследование:**
java.lang.Object
```
public class OutlineOptions
```

Позволяет указать параметры контура.

 Чтобы узнать больше, посетите**Save a Document** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBookmarksOutlineLevels()](#getBookmarksOutlineLevels--) | Позволяет указать уровень контура отдельных закладок. |
| [getClass()](#getClass--) |  |
| [getCreateMissingOutlineLevels()](#getCreateMissingOutlineLevels--) | Получает или задает значение, определяющее, создавать ли отсутствующие уровни структуры при экспорте документа. |
| [getCreateOutlinesForHeadingsInTables()](#getCreateOutlinesForHeadingsInTables--) | Указывает, создавать ли контуры для заголовков (абзацев, отформатированных с помощью стилей заголовков) внутри таблиц. |
| [getDefaultBookmarksOutlineLevel()](#getDefaultBookmarksOutlineLevel--) | Указывает уровень по умолчанию в структуре документа, на котором должны отображаться закладки Word. |
| [getExpandedOutlineLevels()](#getExpandedOutlineLevels--) | Указывает, сколько уровней в структуре документа должно отображаться в развернутом виде при просмотре файла. |
| [getHeadingsOutlineLevels()](#getHeadingsOutlineLevels--) | Указывает, сколько уровней заголовков (абзацев, отформатированных с помощью стилей заголовков) следует включить в структуру документа. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setCreateMissingOutlineLevels(boolean value)](#setCreateMissingOutlineLevels-boolean-) | Получает или задает значение, определяющее, создавать ли отсутствующие уровни структуры при экспорте документа. |
| [setCreateOutlinesForHeadingsInTables(boolean value)](#setCreateOutlinesForHeadingsInTables-boolean-) | Указывает, создавать ли контуры для заголовков (абзацев, отформатированных с помощью стилей заголовков) внутри таблиц. |
| [setDefaultBookmarksOutlineLevel(int value)](#setDefaultBookmarksOutlineLevel-int-) | Указывает уровень по умолчанию в структуре документа, на котором должны отображаться закладки Word. |
| [setExpandedOutlineLevels(int value)](#setExpandedOutlineLevels-int-) | Указывает, сколько уровней в структуре документа должно отображаться в развернутом виде при просмотре файла. |
| [setHeadingsOutlineLevels(int value)](#setHeadingsOutlineLevels-int-) | Указывает, сколько уровней заголовков (абзацев, отформатированных с помощью стилей заголовков) следует включить в структуру документа. |
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
### getBookmarksOutlineLevels() {#getBookmarksOutlineLevels--}
```
public BookmarksOutlineLevelCollection getBookmarksOutlineLevels()
```


Позволяет указать уровень контура отдельных закладок.

 Если уровень закладки не указан в этой коллекции, то[getDefaultBookmarksOutlineLevel()](../../com.aspose.words/outlineoptions\#getDefaultBookmarksOutlineLevel--) / [setDefaultBookmarksOutlineLevel(int)](../../com.aspose.words/outlineoptions\#setDefaultBookmarksOutlineLevel-int-) используется значение.

**Возвращает:**
[BookmarksOutlineLevelCollection](../../com.aspose.words/bookmarksoutlinelevelcollection) - соответствующий[BookmarksOutlineLevelCollection](../../com.aspose.words/bookmarksoutlinelevelcollection) ценность.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getCreateMissingOutlineLevels() {#getCreateMissingOutlineLevels--}
```
public boolean getCreateMissingOutlineLevels()
```


Получает или задает значение, определяющее, создавать ли отсутствующие уровни структуры при экспорте документа.

 Значение по умолчанию для этого свойства**false**.

**Возвращает:**
boolean - соответствующее логическое значение.
### getCreateOutlinesForHeadingsInTables() {#getCreateOutlinesForHeadingsInTables--}
```
public boolean getCreateOutlinesForHeadingsInTables()
```


Указывает, создавать ли контуры для заголовков (абзацев, отформатированных с помощью стилей заголовков) внутри таблиц.

 Значение по умолчанию**false**.

**Возвращает:**
boolean - соответствующее логическое значение.
### getDefaultBookmarksOutlineLevel() {#getDefaultBookmarksOutlineLevel--}
```
public int getDefaultBookmarksOutlineLevel()
```


Указывает уровень по умолчанию в структуре документа, на котором должны отображаться закладки Word.

 Уровень отдельных закладок можно указать с помощью[getBookmarksOutlineLevels()](../../com.aspose.words/outlineoptions\#getBookmarksOutlineLevels--) имущество.

Укажите 0, и закладки Word не будут отображаться в структуре документа. Укажите 1, и закладки Word будут отображаться в структуре документа на уровне 1; 2 для уровня 2 и так далее.

Значение по умолчанию — 0. Допустимый диапазон — от 0 до 9.

**Возвращает:**
int - соответствующее значение int.
### getExpandedOutlineLevels() {#getExpandedOutlineLevels--}
```
public int getExpandedOutlineLevels()
```


Указывает, сколько уровней в структуре документа должно отображаться в развернутом виде при просмотре файла.

Обратите внимание, что эти параметры не будут работать при сохранении в XPS.

Укажите 0, и структура документа будет свернута; укажите 1, и элементы первого уровня в структуре будут развернуты и так далее.

Значение по умолчанию — 0. Допустимый диапазон — от 0 до 9.

**Возвращает:**
int - соответствующее значение int.
### getHeadingsOutlineLevels() {#getHeadingsOutlineLevels--}
```
public int getHeadingsOutlineLevels()
```


Указывает, сколько уровней заголовков (абзацев, отформатированных с помощью стилей заголовков) следует включить в структуру документа.

Укажите 0, чтобы в структуре не было заголовков; указать 1 для одного уровня заголовков в структуре и т.д.

Значение по умолчанию — 0. Допустимый диапазон — от 0 до 9.

**Возвращает:**
int - соответствующее значение int.
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




### setCreateMissingOutlineLevels(boolean value) {#setCreateMissingOutlineLevels-boolean-}
```
public void setCreateMissingOutlineLevels(boolean value)
```


Получает или задает значение, определяющее, создавать ли отсутствующие уровни структуры при экспорте документа.

 Значение по умолчанию для этого свойства**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setCreateOutlinesForHeadingsInTables(boolean value) {#setCreateOutlinesForHeadingsInTables-boolean-}
```
public void setCreateOutlinesForHeadingsInTables(boolean value)
```


Указывает, создавать ли контуры для заголовков (абзацев, отформатированных с помощью стилей заголовков) внутри таблиц.

 Значение по умолчанию**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setDefaultBookmarksOutlineLevel(int value) {#setDefaultBookmarksOutlineLevel-int-}
```
public void setDefaultBookmarksOutlineLevel(int value)
```


Указывает уровень по умолчанию в структуре документа, на котором должны отображаться закладки Word.

 Уровень отдельных закладок можно указать с помощью[getBookmarksOutlineLevels()](../../com.aspose.words/outlineoptions\#getBookmarksOutlineLevels--) имущество.

Укажите 0, и закладки Word не будут отображаться в структуре документа. Укажите 1, и закладки Word будут отображаться в структуре документа на уровне 1; 2 для уровня 2 и так далее.

Значение по умолчанию — 0. Допустимый диапазон — от 0 до 9.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее целочисленное значение. |

### setExpandedOutlineLevels(int value) {#setExpandedOutlineLevels-int-}
```
public void setExpandedOutlineLevels(int value)
```


Указывает, сколько уровней в структуре документа должно отображаться в развернутом виде при просмотре файла.

Обратите внимание, что эти параметры не будут работать при сохранении в XPS.

Укажите 0, и структура документа будет свернута; укажите 1, и элементы первого уровня в структуре будут развернуты и так далее.

Значение по умолчанию — 0. Допустимый диапазон — от 0 до 9.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее целочисленное значение. |

### setHeadingsOutlineLevels(int value) {#setHeadingsOutlineLevels-int-}
```
public void setHeadingsOutlineLevels(int value)
```


Указывает, сколько уровней заголовков (абзацев, отформатированных с помощью стилей заголовков) следует включить в структуру документа.

Укажите 0, чтобы в структуре не было заголовков; указать 1 для одного уровня заголовков в структуре и т.д.

Значение по умолчанию — 0. Допустимый диапазон — от 0 до 9.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее целочисленное значение. |

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
