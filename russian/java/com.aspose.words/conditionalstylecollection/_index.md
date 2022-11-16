---
title: ConditionalStyleCollection
second_title: Справочник по API Aspose.Words для Java
description: Представляет коллекцию объектов.
type: docs
weight: 90
url: /ru/java/com.aspose.words/conditionalstylecollection/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Iterable
```
public class ConditionalStyleCollection implements Iterable
```

 Представляет собой совокупность[ConditionalStyle](../../com.aspose.words/conditionalstyle) объекты.

 Чтобы узнать больше, посетите**Working with Tables** документальная статья.

 Добавить или удалить элементы из этой коллекции невозможно. Он содержит постоянный набор элементов: по одному элементу для каждого значения[ConditionalStyleType](../../com.aspose.words/conditionalstyletype) тип перечисления.
## Методы

| Метод | Описание |
| --- | --- |
| [clearFormatting()](#clearFormatting--) | Очищает все условные стили стиля таблицы. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) |  Получает[ConditionalStyle](../../com.aspose.words/conditionalstyle) объект по индексу. |
| [getBottomLeftCell()](#getBottomLeftCell--) | Получает стиль нижней левой ячейки. |
| [getBottomRightCell()](#getBottomRightCell--) | Получает стиль нижней правой ячейки. |
| [getByConditionalStyleType(int conditionalStyleType)](#getByConditionalStyleType-int-) |  |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | Получает количество условных стилей в коллекции. |
| [getEvenColumnBanding()](#getEvenColumnBanding--) | Получает четный стиль чередования столбцов. |
| [getEvenRowBanding()](#getEvenRowBanding--) | Получает четный стиль чередования строк. |
| [getFirstColumn()](#getFirstColumn--) | Получает первый стиль столбца. |
| [getFirstRow()](#getFirstRow--) | Получает стиль первой строки. |
| [getLastColumn()](#getLastColumn--) | Получает стиль последнего столбца. |
| [getLastRow()](#getLastRow--) | Получает стиль последней строки. |
| [getOddColumnBanding()](#getOddColumnBanding--) | Получает нечетный стиль чередования столбцов. |
| [getOddRowBanding()](#getOddRowBanding--) | Получает стиль чередования нечетных строк. |
| [getTopLeftCell()](#getTopLeftCell--) | Получает стиль верхней левой ячейки. |
| [getTopRightCell()](#getTopRightCell--) | Получает стиль верхней правой ячейки. |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | Возвращает объект перечислителя, который можно использовать для перебора всех условных стилей в коллекции. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clearFormatting() {#clearFormatting--}
```
public void clearFormatting()
```


Очищает все условные стили стиля таблицы.

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
### get(int index) {#get-int-}
```
public ConditionalStyle get(int index)
```


 Получает[ConditionalStyle](../../com.aspose.words/conditionalstyle) объект по индексу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Отсчитываемый от нуля индекс условного стиля для извлечения. |

**Возвращает:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle) - соответствующий[ConditionalStyle](../../com.aspose.words/conditionalstyle) ценность.
### getBottomLeftCell() {#getBottomLeftCell--}
```
public ConditionalStyle getBottomLeftCell()
```


Получает стиль нижней левой ячейки.

**Возвращает:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle) - Нижний левый стиль ячейки.
### getBottomRightCell() {#getBottomRightCell--}
```
public ConditionalStyle getBottomRightCell()
```


Получает стиль нижней правой ячейки.

**Возвращает:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle) - Стиль нижней правой ячейки.
### getByConditionalStyleType(int conditionalStyleType) {#getByConditionalStyleType-int-}
```
public ConditionalStyle getByConditionalStyleType(int conditionalStyleType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| conditionalStyleType | int |  |

**Возвращает:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle)
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getCount() {#getCount--}
```
public int getCount()
```


Получает количество условных стилей в коллекции.

**Возвращает:**
int — количество условных стилей в коллекции.
### getEvenColumnBanding() {#getEvenColumnBanding--}
```
public ConditionalStyle getEvenColumnBanding()
```


Получает четный стиль чередования столбцов.

**Возвращает:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle) - Равномерный стиль обвязки столбцов.
### getEvenRowBanding() {#getEvenRowBanding--}
```
public ConditionalStyle getEvenRowBanding()
```


Получает четный стиль чередования строк.

**Возвращает:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle) - Равномерный стиль обвязки строк.
### getFirstColumn() {#getFirstColumn--}
```
public ConditionalStyle getFirstColumn()
```


Получает первый стиль столбца.

**Возвращает:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle) - Стиль первой колонки.
### getFirstRow() {#getFirstRow--}
```
public ConditionalStyle getFirstRow()
```


Получает стиль первой строки.

**Возвращает:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle) - Стиль первой строки.
### getLastColumn() {#getLastColumn--}
```
public ConditionalStyle getLastColumn()
```


Получает стиль последнего столбца.

**Возвращает:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle) - Стиль последней колонки.
### getLastRow() {#getLastRow--}
```
public ConditionalStyle getLastRow()
```


Получает стиль последней строки.

**Возвращает:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle) - Стиль последней строки.
### getOddColumnBanding() {#getOddColumnBanding--}
```
public ConditionalStyle getOddColumnBanding()
```


Получает нечетный стиль чередования столбцов.

**Возвращает:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle) - Нечетный стиль объединения столбцов.
### getOddRowBanding() {#getOddRowBanding--}
```
public ConditionalStyle getOddRowBanding()
```


Получает стиль чередования нечетных строк.

**Возвращает:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle) - Стиль объединения нечетных рядов.
### getTopLeftCell() {#getTopLeftCell--}
```
public ConditionalStyle getTopLeftCell()
```


Получает стиль верхней левой ячейки.

**Возвращает:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle) - Стиль верхней левой ячейки.
### getTopRightCell() {#getTopRightCell--}
```
public ConditionalStyle getTopRightCell()
```


Получает стиль верхней правой ячейки.

**Возвращает:**
[ConditionalStyle](../../com.aspose.words/conditionalstyle) - Стиль верхней правой ячейки.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### iterator() {#iterator--}
```
public Iterator iterator()
```


Возвращает объект перечислителя, который можно использовать для перебора всех условных стилей в коллекции.

**Возвращает:**
java.util.Iterator
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
