---
title: BorderCollection
second_title: Справочник по API Aspose.Words для Java
description: Коллекция объектов Border.
type: docs
weight: 37
url: /ru/java/com.aspose.words/bordercollection/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Iterable
```
public class BorderCollection implements Iterable
```

Коллекция объектов Border.

 Чтобы узнать больше, посетите**Programming with Documents** документальная статья.

Различные элементы документа имеют разные границы. Например, ParagraphFormat имеет нижнюю, левую, правую и верхнюю границы. Вы можете указать различное форматирование для каждой границы независимо или перечислить все границы и применить одинаковое форматирование.
## Методы

| Метод | Описание |
| --- | --- |
| [clearFormatting()](#clearFormatting--) | Удаляет все границы объекта. |
| [equals(BorderCollection brColl)](#equals-com.aspose.words.BorderCollection-) | Сравнивает наборы бордюров. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | Извлекает объект Border по индексу. |
| [getBottom()](#getBottom--) | Получает нижнюю границу. |
| [getByBorderType(int borderType)](#getByBorderType-int-) |  |
| [getClass()](#getClass--) |  |
| [getColor()](#getColor--) | Получает цвет границы. |
| [getCount()](#getCount--) | Получает количество границ в коллекции. |
| [getDistanceFromText()](#getDistanceFromText--) | Получает расстояние границы от текста в пунктах. |
| [getHorizontal()](#getHorizontal--) | Получает горизонтальную границу, используемую между ячейками или соответствующими абзацами. |
| [getLeft()](#getLeft--) | Получает левую границу. |
| [getLineStyle()](#getLineStyle--) | Получает стиль границы. |
| [getLineWidth()](#getLineWidth--) | Получает ширину границы в пунктах. |
| [getRight()](#getRight--) | Получает правильную границу. |
| [getShadow()](#getShadow--) | Получает значение, указывающее, есть ли у границы тень. |
| [getTop()](#getTop--) | Получает верхнюю границу. |
| [getVertical()](#getVertical--) | Получает вертикальную границу, используемую между ячейками. |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | Возвращает объект перечислителя, который можно использовать для перебора всех границ в коллекции. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setColor(Color value)](#setColor-java.awt.Color-) | Задает цвет границы. |
| [setDistanceFromText(double value)](#setDistanceFromText-double-) | Устанавливает расстояние границы от текста в пунктах. |
| [setLineStyle(int value)](#setLineStyle-int-) | Устанавливает стиль границы. |
| [setLineWidth(double value)](#setLineWidth-double-) | Устанавливает ширину границы в пунктах. |
| [setShadow(boolean value)](#setShadow-boolean-) | Задает значение, указывающее, есть ли у границы тень. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clearFormatting() {#clearFormatting--}
```
public void clearFormatting()
```


Удаляет все границы объекта.

### equals(BorderCollection brColl) {#equals-com.aspose.words.BorderCollection-}
```
public boolean equals(BorderCollection brColl)
```


Сравнивает наборы бордюров.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| brColl | [BorderCollection](../../com.aspose.words/bordercollection) |  |

**Возвращает:**
логический
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
public Border get(int index)
```


Извлекает объект Border по индексу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Отсчитываемый от нуля индекс границы для извлечения. |

**Возвращает:**
[Border](../../com.aspose.words/border) - соответствующий[Border](../../com.aspose.words/border) ценность.
### getBottom() {#getBottom--}
```
public Border getBottom()
```


Получает нижнюю границу.

**Возвращает:**
[Border](../../com.aspose.words/border) - Нижняя граница.
### getByBorderType(int borderType) {#getByBorderType-int-}
```
public Border getByBorderType(int borderType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| borderType | int |  |

**Возвращает:**
[Border](../../com.aspose.words/border)
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getColor() {#getColor--}
```
public Color getColor()
```


Получает цвет границы.

Возвращает цвет первой границы в коллекции.

Задает цвет всех границ в коллекции, кроме диагональных границ.

**Возвращает:**
java.awt.Color — цвет границы.
### getCount() {#getCount--}
```
public int getCount()
```


Получает количество границ в коллекции.

**Возвращает:**
int - количество границ в коллекции.
### getDistanceFromText() {#getDistanceFromText--}
```
public double getDistanceFromText()
```


Получает расстояние границы от текста в пунктах.

Получает расстояние от текста для первой границы.

Задает расстояние от текста для всех границ в коллекции, кроме диагональных границ.

Не имеет никакого эффекта и будет автоматически обнулен для границ ячеек таблицы.

**Возвращает:**
double - Расстояние границы от текста в пунктах.
### getHorizontal() {#getHorizontal--}
```
public Border getHorizontal()
```


Получает горизонтальную границу, используемую между ячейками или соответствующими абзацами.

**Возвращает:**
[Border](../../com.aspose.words/border) - Горизонтальная граница, используемая между ячейками или соответствующими абзацами.
### getLeft() {#getLeft--}
```
public Border getLeft()
```


Получает левую границу.

**Возвращает:**
[Border](../../com.aspose.words/border) - Левая граница.
### getLineStyle() {#getLineStyle--}
```
public int getLineStyle()
```


Получает стиль границы.

Возвращает стиль первой рамки в коллекции.

Устанавливает стиль всех границ в коллекции, кроме диагональных границ.

**Возвращает:**
int - Стиль границы. Возвращаемое значение является одним из[LineStyle](../../com.aspose.words/linestyle) константы.
### getLineWidth() {#getLineWidth--}
```
public double getLineWidth()
```


Получает ширину границы в пунктах.

Возвращает ширину первой границы в коллекции.

Устанавливает ширину всех границ в коллекции, кроме диагональных границ.

**Возвращает:**
double - Ширина границы в пунктах.
### getRight() {#getRight--}
```
public Border getRight()
```


Получает правильную границу.

**Возвращает:**
[Border](../../com.aspose.words/border) - Правая граница.
### getShadow() {#getShadow--}
```
public boolean getShadow()
```


Получает значение, указывающее, есть ли у границы тень.

Получает значение от первой границы в коллекции.

Задает значение для всех границ в коллекции, кроме диагональных границ.

**Возвращает:**
boolean — значение, указывающее, есть ли у границы тень.
### getTop() {#getTop--}
```
public Border getTop()
```


Получает верхнюю границу.

**Возвращает:**
[Border](../../com.aspose.words/border) - Верхняя граница.
### getVertical() {#getVertical--}
```
public Border getVertical()
```


Получает вертикальную границу, используемую между ячейками.

**Возвращает:**
[Border](../../com.aspose.words/border) - Вертикальная граница, используемая между ячейками.
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


Возвращает объект перечислителя, который можно использовать для перебора всех границ в коллекции.

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




### setColor(Color value) {#setColor-java.awt.Color-}
```
public void setColor(Color value)
```


Задает цвет границы.

Возвращает цвет первой границы в коллекции.

Задает цвет всех границ в коллекции, кроме диагональных границ.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.awt.Color | Цвет границы. |

### setDistanceFromText(double value) {#setDistanceFromText-double-}
```
public void setDistanceFromText(double value)
```


Устанавливает расстояние границы от текста в пунктах.

Получает расстояние от текста для первой границы.

Задает расстояние от текста для всех границ в коллекции, кроме диагональных границ.

Не имеет никакого эффекта и будет автоматически обнулен для границ ячеек таблицы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Расстояние границы от текста в пунктах. |

### setLineStyle(int value) {#setLineStyle-int-}
```
public void setLineStyle(int value)
```


Устанавливает стиль границы.

Возвращает стиль первой рамки в коллекции.

Устанавливает стиль всех границ в коллекции, кроме диагональных границ.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Стиль границы. Значение должно быть одним из[LineStyle](../../com.aspose.words/linestyle) константы. |

### setLineWidth(double value) {#setLineWidth-double-}
```
public void setLineWidth(double value)
```


Устанавливает ширину границы в пунктах.

Возвращает ширину первой границы в коллекции.

Устанавливает ширину всех границ в коллекции, кроме диагональных границ.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Ширина границы в пунктах. |

### setShadow(boolean value) {#setShadow-boolean-}
```
public void setShadow(boolean value)
```


Задает значение, указывающее, есть ли у границы тень.

Получает значение от первой границы в коллекции.

Задает значение для всех границ в коллекции, кроме диагональных границ.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, указывающее, есть ли у границы тень. |

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
