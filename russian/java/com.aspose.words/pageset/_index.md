---
title: PageSet
second_title: Справочник по API Aspose.Words для Java
description: Описывает случайный набор страниц.
type: docs
weight: 439
url: /ru/java/com.aspose.words/pageset/
---

**Наследование:**
java.lang.Object
```
public class PageSet
```

Описывает случайный набор страниц.

 Чтобы узнать больше, посетите**Programming with Documents** документальная статья.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [PageSet(int page)](#PageSet-int-) | Создает одностраничный набор на основе точного индекса страницы. |
| [PageSet(int[] pages)](#PageSet-int...-) | Создает набор страниц на основе точных индексов страниц. |
| [PageSet(PageRange[] ranges)](#PageSet-com.aspose.words.PageRange...-) | Создает набор страниц на основе диапазонов. |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAll()](#getAll--) | Получает набор со всеми страницами документа в их исходном порядке. |
| [getClass()](#getClass--) |  |
| [getEven()](#getEven--) | Получает набор со всеми четными страницами документа в их исходном порядке. |
| [getOdd()](#getOdd--) | Получает набор со всеми нечетными страницами документа в их исходном порядке. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### PageSet(int page) {#PageSet-int-}
```
public PageSet(int page)
```


Создает одностраничный набор на основе точного индекса страницы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| page | int | Нулевой индекс страницы. Если встречается страница, которой нет в документе, во время рендеринга будет выдано исключение. означает последнюю страницу в документе. |

### PageSet(int[] pages) {#PageSet-int...-}
```
public PageSet(int[] pages)
```


Создает набор страниц на основе точных индексов страниц.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| pages | int[] | Отсчитываемые от нуля индексы страниц. Если встречается страница, которой нет в документе, во время рендеринга будет выдано исключение. означает последнюю страницу в документе. |

### PageSet(PageRange[] ranges) {#PageSet-com.aspose.words.PageRange...-}
```
public PageSet(PageRange[] ranges)
```


Создает набор страниц на основе диапазонов.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| ranges | [PageRange\[\]](../../com.aspose.words/pagerange) | Массив диапазонов страниц. Если встречается диапазон, который начинается после последней страницы в документе, во время рендеринга будет выдано исключение. Все диапазоны, которые заканчиваются после последней страницы, усекаются, чтобы поместиться в документе. |

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
### getAll() {#getAll--}
```
public static PageSet getAll()
```


Получает набор со всеми страницами документа в их исходном порядке.

**Возвращает:**
[PageSet](../../com.aspose.words/pageset) - Набор со всеми страницами документа в их первоначальном порядке.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getEven() {#getEven--}
```
public static PageSet getEven()
```


Получает набор со всеми четными страницами документа в их исходном порядке. Четные страницы имеют нечетные индексы, поскольку индексы страниц отсчитываются от нуля.

**Возвращает:**
[PageSet](../../com.aspose.words/pageset) - Набор со всеми четными страницами документа в их первоначальном порядке.
### getOdd() {#getOdd--}
```
public static PageSet getOdd()
```


Получает набор со всеми нечетными страницами документа в их исходном порядке. Нечетные страницы имеют четные индексы, поскольку индексы страниц отсчитываются от нуля.

**Возвращает:**
[PageSet](../../com.aspose.words/pageset) - Набор со всеми нечетными страницами документа в их первоначальном порядке.
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
