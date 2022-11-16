---
title: Stroke
second_title: Справочник по API Aspose.Words для Java
description: Определяет штрих для фигуры.
type: docs
weight: 531
url: /ru/java/com.aspose.words/stroke/
---

**Наследование:**
java.lang.Object
```
public class Stroke
```

Определяет штрих для фигуры.

 Чтобы узнать больше, посетите**Working with Shapes** документальная статья.

 Использовать[Shape.getStroke()](../../com.aspose.words/shape\#getStroke--) для доступа к свойствам обводки фигуры. Вы не создаете экземпляры[Stroke](../../com.aspose.words/stroke) класс напрямую.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBackColor()](#getBackColor--) | Получает цвет фона обводки. |
| [getClass()](#getClass--) |  |
| [getColor()](#getColor--) | Определяет цвет обводки. |
| [getColor2()](#getColor2--) | Определяет второй цвет для обводки. |
| [getDashStyle()](#getDashStyle--) | Указывает шаблон точки и штриха для штриха. |
| [getEndArrowLength()](#getEndArrowLength--) | Определяет длину стрелки для конца штриха. |
| [getEndArrowType()](#getEndArrowType--) | Определяет наконечник стрелки для конца штриха. |
| [getEndArrowWidth()](#getEndArrowWidth--) | Определяет ширину наконечника стрелки для конца штриха. |
| [getEndCap()](#getEndCap--) | Определяет стиль окончания штриха. |
| [getForeColor()](#getForeColor--) | Получает цвет переднего плана обводки. |
| [getImageBytes()](#getImageBytes--) | Определяет изображение для штрихового изображения или заливки узором. |
| [getJoinStyle()](#getJoinStyle--) | Определяет стиль соединения полилинии. |
| [getLineStyle()](#getLineStyle--) | Определяет стиль линии штриха. |
| [getOn()](#getOn--) | Определяет, будет ли контур обведен. |
| [getOpacity()](#getOpacity--) | Определяет степень прозрачности штриха. |
| [getStartArrowLength()](#getStartArrowLength--) | Определяет длину стрелки для начала штриха. |
| [getStartArrowType()](#getStartArrowType--) | Определяет наконечник стрелки для начала штриха. |
| [getStartArrowWidth()](#getStartArrowWidth--) | Определяет ширину наконечника стрелки для начала штриха. |
| [getTransparency()](#getTransparency--) | Получает значение от 0,0 (непрозрачный) до 1,0 (прозрачный), представляющее степень прозрачности обводки. |
| [getVisible()](#getVisible--) | Получает флаг, указывающий, виден ли штрих. |
| [getWeight()](#getWeight--) | Определяет толщину кисти, которая обводит контур фигуры в точках. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setBackColor(Color value)](#setBackColor-java.awt.Color-) | Устанавливает цвет фона обводки. |
| [setColor(Color value)](#setColor-java.awt.Color-) | Определяет цвет обводки. |
| [setColor2(Color value)](#setColor2-java.awt.Color-) | Определяет второй цвет для обводки. |
| [setDashStyle(int value)](#setDashStyle-int-) | Указывает шаблон точки и штриха для штриха. |
| [setEndArrowLength(int value)](#setEndArrowLength-int-) | Определяет длину стрелки для конца штриха. |
| [setEndArrowType(int value)](#setEndArrowType-int-) | Определяет наконечник стрелки для конца штриха. |
| [setEndArrowWidth(int value)](#setEndArrowWidth-int-) | Определяет ширину наконечника стрелки для конца штриха. |
| [setEndCap(int value)](#setEndCap-int-) | Определяет стиль окончания штриха. |
| [setForeColor(Color value)](#setForeColor-java.awt.Color-) | Устанавливает цвет переднего плана обводки. |
| [setJoinStyle(int value)](#setJoinStyle-int-) | Определяет стиль соединения полилинии. |
| [setLineStyle(int value)](#setLineStyle-int-) | Определяет стиль линии штриха. |
| [setOn(boolean value)](#setOn-boolean-) | Определяет, будет ли контур обведен. |
| [setOpacity(double value)](#setOpacity-double-) | Определяет степень прозрачности штриха. |
| [setStartArrowLength(int value)](#setStartArrowLength-int-) | Определяет длину стрелки для начала штриха. |
| [setStartArrowType(int value)](#setStartArrowType-int-) | Определяет наконечник стрелки для начала штриха. |
| [setStartArrowWidth(int value)](#setStartArrowWidth-int-) | Определяет ширину наконечника стрелки для начала штриха. |
| [setTransparency(double value)](#setTransparency-double-) | Задает значение от 0,0 (непрозрачный) до 1,0 (прозрачный), представляющее степень прозрачности штриха. |
| [setVisible(boolean value)](#setVisible-boolean-) | Устанавливает флаг, указывающий, виден ли штрих. |
| [setWeight(double value)](#setWeight-double-) | Определяет толщину кисти, которая обводит контур фигуры в точках. |
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
### getBackColor() {#getBackColor--}
```
public Color getBackColor()
```


 Получает цвет фона обводки. Значение по умолчанию для[Shape](../../com.aspose.words/shape) является .

**Возвращает:**
java.awt.Color — цвет фона обводки.
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


Определяет цвет обводки.

 Значение по умолчанию для[Shape](../../com.aspose.words/shape) является .

**Возвращает:**
java.awt.Color — соответствующее значение java.awt.Color.
### getColor2() {#getColor2--}
```
public Color getColor2()
```


Определяет второй цвет для обводки.

 Значение по умолчанию для[Shape](../../com.aspose.words/shape) является .

**Возвращает:**
java.awt.Color — соответствующее значение java.awt.Color.
### getDashStyle() {#getDashStyle--}
```
public int getDashStyle()
```


Указывает шаблон точки и штриха для штриха.

 Значение по умолчанию[DashStyle.SOLID](../../com.aspose.words/dashstyle\#SOLID).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[DashStyle](../../com.aspose.words/dashstyle) константы.
### getEndArrowLength() {#getEndArrowLength--}
```
public int getEndArrowLength()
```


Определяет длину стрелки для конца штриха.

 Значение по умолчанию[ArrowLength.MEDIUM](../../com.aspose.words/arrowlength\#MEDIUM).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[ArrowLength](../../com.aspose.words/arrowlength) константы.
### getEndArrowType() {#getEndArrowType--}
```
public int getEndArrowType()
```


Определяет наконечник стрелки для конца штриха.

 Значение по умолчанию[ArrowType.NONE](../../com.aspose.words/arrowtype\#NONE).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[ArrowType](../../com.aspose.words/arrowtype) константы.
### getEndArrowWidth() {#getEndArrowWidth--}
```
public int getEndArrowWidth()
```


Определяет ширину наконечника стрелки для конца штриха.

 Значение по умолчанию[ArrowWidth.MEDIUM](../../com.aspose.words/arrowwidth\#MEDIUM).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[ArrowWidth](../../com.aspose.words/arrowwidth) константы.
### getEndCap() {#getEndCap--}
```
public int getEndCap()
```


Определяет стиль окончания штриха.

 Значение по умолчанию[EndCap.FLAT](../../com.aspose.words/endcap\#FLAT).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[EndCap](../../com.aspose.words/endcap) константы.
### getForeColor() {#getForeColor--}
```
public Color getForeColor()
```


 Получает цвет переднего плана обводки. Значение по умолчанию для[Shape](../../com.aspose.words/shape) является .

**Возвращает:**
java.awt.Color — цвет переднего плана штриха.
### getImageBytes() {#getImageBytes--}
```
public byte[] getImageBytes()
```


Определяет изображение для штрихового изображения или заливки узором.

**Возвращает:**
байт[] - соответствующий байт[] ценность.
### getJoinStyle() {#getJoinStyle--}
```
public int getJoinStyle()
```


Определяет стиль соединения полилинии.

 Значение по умолчанию[JoinStyle.ROUND](../../com.aspose.words/joinstyle\#ROUND).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[JoinStyle](../../com.aspose.words/joinstyle) константы.
### getLineStyle() {#getLineStyle--}
```
public int getLineStyle()
```


Определяет стиль линии штриха.

 Значение по умолчанию[ShapeLineStyle.SINGLE](../../com.aspose.words/shapelinestyle\#SINGLE).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[ShapeLineStyle](../../com.aspose.words/shapelinestyle) константы.
### getOn() {#getOn--}
```
public boolean getOn()
```


Определяет, будет ли контур обведен.

 Значение по умолчанию для[Shape](../../com.aspose.words/shape) является**true**.

**Возвращает:**
boolean - соответствующее логическое значение.
### getOpacity() {#getOpacity--}
```
public double getOpacity()
```


Определяет степень прозрачности штриха. Допустимый диапазон от 0 до 1.

Значение по умолчанию — 1.

**Возвращает:**
double - соответствующее двойное значение.
### getStartArrowLength() {#getStartArrowLength--}
```
public int getStartArrowLength()
```


Определяет длину стрелки для начала штриха.

 Значение по умолчанию[ArrowLength.MEDIUM](../../com.aspose.words/arrowlength\#MEDIUM).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[ArrowLength](../../com.aspose.words/arrowlength) константы.
### getStartArrowType() {#getStartArrowType--}
```
public int getStartArrowType()
```


Определяет наконечник стрелки для начала штриха.

 Значение по умолчанию[ArrowType.NONE](../../com.aspose.words/arrowtype\#NONE).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[ArrowType](../../com.aspose.words/arrowtype) константы.
### getStartArrowWidth() {#getStartArrowWidth--}
```
public int getStartArrowWidth()
```


Определяет ширину наконечника стрелки для начала штриха.

 Значение по умолчанию[ArrowWidth.MEDIUM](../../com.aspose.words/arrowwidth\#MEDIUM).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[ArrowWidth](../../com.aspose.words/arrowwidth) константы.
### getTransparency() {#getTransparency--}
```
public double getTransparency()
```


Получает значение от 0,0 (непрозрачный) до 1,0 (прозрачный), представляющее степень прозрачности обводки. Значение по умолчанию — 0.

**Возвращает:**
double — значение от 0,0 (непрозрачный) до 1,0 (прозрачный), представляющее степень прозрачности штриха.
### getVisible() {#getVisible--}
```
public boolean getVisible()
```


 Получает флаг, указывающий, виден ли штрих. Значение по умолчанию для[Shape](../../com.aspose.words/shape) является**true**.

**Возвращает:**
boolean — Флаг, указывающий, виден ли штрих.
### getWeight() {#getWeight--}
```
public double getWeight()
```


Определяет толщину кисти, которая обводит контур фигуры в точках.

 Значение по умолчанию для[Shape](../../com.aspose.words/shape) составляет 0,75.

**Возвращает:**
double - соответствующее двойное значение.
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




### setBackColor(Color value) {#setBackColor-java.awt.Color-}
```
public void setBackColor(Color value)
```


 Устанавливает цвет фона обводки. Значение по умолчанию для[Shape](../../com.aspose.words/shape) является .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.awt.Color | Цвет фона обводки. |

### setColor(Color value) {#setColor-java.awt.Color-}
```
public void setColor(Color value)
```


Определяет цвет обводки.

 Значение по умолчанию для[Shape](../../com.aspose.words/shape) является .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.awt.Color | Соответствующее значение java.awt.Color. |

### setColor2(Color value) {#setColor2-java.awt.Color-}
```
public void setColor2(Color value)
```


Определяет второй цвет для обводки.

 Значение по умолчанию для[Shape](../../com.aspose.words/shape) является .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.awt.Color | Соответствующее значение java.awt.Color. |

### setDashStyle(int value) {#setDashStyle-int-}
```
public void setDashStyle(int value)
```


Указывает шаблон точки и штриха для штриха.

 Значение по умолчанию[DashStyle.SOLID](../../com.aspose.words/dashstyle\#SOLID).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[DashStyle](../../com.aspose.words/dashstyle) константы. |

### setEndArrowLength(int value) {#setEndArrowLength-int-}
```
public void setEndArrowLength(int value)
```


Определяет длину стрелки для конца штриха.

 Значение по умолчанию[ArrowLength.MEDIUM](../../com.aspose.words/arrowlength\#MEDIUM).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[ArrowLength](../../com.aspose.words/arrowlength) константы. |

### setEndArrowType(int value) {#setEndArrowType-int-}
```
public void setEndArrowType(int value)
```


Определяет наконечник стрелки для конца штриха.

 Значение по умолчанию[ArrowType.NONE](../../com.aspose.words/arrowtype\#NONE).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[ArrowType](../../com.aspose.words/arrowtype) константы. |

### setEndArrowWidth(int value) {#setEndArrowWidth-int-}
```
public void setEndArrowWidth(int value)
```


Определяет ширину наконечника стрелки для конца штриха.

 Значение по умолчанию[ArrowWidth.MEDIUM](../../com.aspose.words/arrowwidth\#MEDIUM).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[ArrowWidth](../../com.aspose.words/arrowwidth) константы. |

### setEndCap(int value) {#setEndCap-int-}
```
public void setEndCap(int value)
```


Определяет стиль окончания штриха.

 Значение по умолчанию[EndCap.FLAT](../../com.aspose.words/endcap\#FLAT).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[EndCap](../../com.aspose.words/endcap) константы. |

### setForeColor(Color value) {#setForeColor-java.awt.Color-}
```
public void setForeColor(Color value)
```


 Устанавливает цвет переднего плана обводки. Значение по умолчанию для[Shape](../../com.aspose.words/shape) является .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.awt.Color | Цвет переднего плана штриха. |

### setJoinStyle(int value) {#setJoinStyle-int-}
```
public void setJoinStyle(int value)
```


Определяет стиль соединения полилинии.

 Значение по умолчанию[JoinStyle.ROUND](../../com.aspose.words/joinstyle\#ROUND).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[JoinStyle](../../com.aspose.words/joinstyle) константы. |

### setLineStyle(int value) {#setLineStyle-int-}
```
public void setLineStyle(int value)
```


Определяет стиль линии штриха.

 Значение по умолчанию[ShapeLineStyle.SINGLE](../../com.aspose.words/shapelinestyle\#SINGLE).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[ShapeLineStyle](../../com.aspose.words/shapelinestyle) константы. |

### setOn(boolean value) {#setOn-boolean-}
```
public void setOn(boolean value)
```


Определяет, будет ли контур обведен.

 Значение по умолчанию для[Shape](../../com.aspose.words/shape) является**true**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setOpacity(double value) {#setOpacity-double-}
```
public void setOpacity(double value)
```


Определяет степень прозрачности штриха. Допустимый диапазон от 0 до 1.

Значение по умолчанию — 1.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Соответствующее двойное значение. |

### setStartArrowLength(int value) {#setStartArrowLength-int-}
```
public void setStartArrowLength(int value)
```


Определяет длину стрелки для начала штриха.

 Значение по умолчанию[ArrowLength.MEDIUM](../../com.aspose.words/arrowlength\#MEDIUM).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[ArrowLength](../../com.aspose.words/arrowlength) константы. |

### setStartArrowType(int value) {#setStartArrowType-int-}
```
public void setStartArrowType(int value)
```


Определяет наконечник стрелки для начала штриха.

 Значение по умолчанию[ArrowType.NONE](../../com.aspose.words/arrowtype\#NONE).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[ArrowType](../../com.aspose.words/arrowtype) константы. |

### setStartArrowWidth(int value) {#setStartArrowWidth-int-}
```
public void setStartArrowWidth(int value)
```


Определяет ширину наконечника стрелки для начала штриха.

 Значение по умолчанию[ArrowWidth.MEDIUM](../../com.aspose.words/arrowwidth\#MEDIUM).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[ArrowWidth](../../com.aspose.words/arrowwidth) константы. |

### setTransparency(double value) {#setTransparency-double-}
```
public void setTransparency(double value)
```


Задает значение от 0,0 (непрозрачный) до 1,0 (прозрачный), представляющее степень прозрачности штриха. Значение по умолчанию — 0.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Значение от 0,0 (непрозрачный) до 1,0 (прозрачный), представляющее степень прозрачности штриха. |

### setVisible(boolean value) {#setVisible-boolean-}
```
public void setVisible(boolean value)
```


Устанавливает флаг, указывающий, виден ли штрих. Значение по умолчанию для[Shape](../../com.aspose.words/shape) является**true**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Флаг, указывающий, виден ли штрих. |

### setWeight(double value) {#setWeight-double-}
```
public void setWeight(double value)
```


Определяет толщину кисти, которая обводит контур фигуры в точках.

 Значение по умолчанию для[Shape](../../com.aspose.words/shape) составляет 0,75.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Соответствующее двойное значение. |

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
