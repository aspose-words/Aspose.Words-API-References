---
title: Bookmark
second_title: Справочник по API Aspose.Words для Java
description: Представляет одну закладку.
type: docs
weight: 31
url: /ru/java/com.aspose.words/bookmark/
---

**Наследование:**
java.lang.Object
```
public class Bookmark
```

Представляет одну закладку.

 Чтобы узнать больше, посетите**Working with Bookmarks** документальная статья.

[Bookmark](../../com.aspose.words/bookmark) это объект «фасад», который инкапсулирует два узла[getBookmarkStart()](../../com.aspose.words/bookmark\#getBookmarkStart--) а также[getBookmarkEnd()](../../com.aspose.words/bookmark\#getBookmarkEnd--)в дереве документа и позволяет работать с закладкой как с единым объектом.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBookmarkEnd()](#getBookmarkEnd--) | Получает узел, представляющий конец закладки. |
| [getBookmarkStart()](#getBookmarkStart--) | Получает узел, представляющий начало закладки. |
| [getClass()](#getClass--) |  |
| [getFirstColumn()](#getFirstColumn--) | Получает отсчитываемый от нуля индекс первого столбца диапазона столбцов таблицы, связанного с закладкой. |
| [getLastColumn()](#getLastColumn--) | Получает отсчитываемый от нуля индекс последнего столбца диапазона столбцов таблицы, связанного с закладкой. |
| [getName()](#getName--) | Получает имя закладки. |
| [getText()](#getText--) | Получает текст, заключенный в закладке. |
| [hashCode()](#hashCode--) |  |
| [isColumn()](#isColumn--) |  Возвращает**true** если эта закладка является закладкой столбца таблицы. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove()](#remove--) | Удаляет закладку из документа. |
| [setName(String value)](#setName-java.lang.String-) | Устанавливает имя закладки. |
| [setText(String value)](#setText-java.lang.String-) | Устанавливает текст, заключенный в закладку. |
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
### getBookmarkEnd() {#getBookmarkEnd--}
```
public BookmarkEnd getBookmarkEnd()
```


Получает узел, представляющий конец закладки.

**Возвращает:**
[BookmarkEnd](../../com.aspose.words/bookmarkend) - Узел, представляющий конец закладки.
### getBookmarkStart() {#getBookmarkStart--}
```
public BookmarkStart getBookmarkStart()
```


Получает узел, представляющий начало закладки.

**Возвращает:**
[BookmarkStart](../../com.aspose.words/bookmarkstart) - Узел, представляющий начало закладки.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getFirstColumn() {#getFirstColumn--}
```
public int getFirstColumn()
```


 Получает отсчитываемый от нуля индекс первого столбца диапазона столбцов таблицы, связанного с закладкой. Возвращает**-1** если эта закладка не является закладкой столбца таблицы.

**Возвращает:**
int — Отсчитываемый от нуля индекс первого столбца диапазона столбцов таблицы, связанного с закладкой.
### getLastColumn() {#getLastColumn--}
```
public int getLastColumn()
```


 Получает отсчитываемый от нуля индекс последнего столбца диапазона столбцов таблицы, связанного с закладкой. Возвращает**-1** если эта закладка не является закладкой столбца таблицы.

**Возвращает:**
int — Отсчитываемый от нуля индекс последнего столбца диапазона столбцов таблицы, связанного с закладкой.
### getName() {#getName--}
```
public String getName()
```


Получает имя закладки. Обратите внимание, что если вы измените имя закладки на имя, которое уже существует в документе, ошибка не будет выдана, и при сохранении документа будет сохранена только первая закладка.

**Возвращает:**
java.lang.String — Имя закладки.
### getText() {#getText--}
```
public String getText()
```


Получает текст, заключенный в закладке.

**Возвращает:**
java.lang.String — текст, заключенный в закладку.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### isColumn() {#isColumn--}
```
public boolean isColumn()
```


 Возвращает**true** если эта закладка является закладкой столбца таблицы.

**Возвращает:**
 логический -**true** если эта закладка является закладкой столбца таблицы.
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### remove() {#remove--}
```
public void remove()
```


Удаляет закладку из документа. Не удаляет текст внутри закладки.

### setName(String value) {#setName-java.lang.String-}
```
public void setName(String value)
```


Устанавливает имя закладки. Обратите внимание, что если вы измените имя закладки на имя, которое уже существует в документе, ошибка не будет выдана, и при сохранении документа будет сохранена только первая закладка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Название закладки. |

### setText(String value) {#setText-java.lang.String-}
```
public void setText(String value)
```


Устанавливает текст, заключенный в закладку.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Текст заключен в закладку. |

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
