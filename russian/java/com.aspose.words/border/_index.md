---
title: Border
second_title: Справочник по API Aspose.Words для Java
description: Представляет границу объекта.
type: docs
weight: 36
url: /ru/java/com.aspose.words/border/
---

**Наследование:**
java.lang.Object, [com.aspose.words.InternableComplexAttr](../../com.aspose.words/internablecomplexattr)

**Все реализованные интерфейсы:**
java.lang.Cloneable
```
public class Border extends InternableComplexAttr implements Cloneable
```

Представляет границу объекта.

 Чтобы узнать больше, посетите**Programming with Documents** документальная статья.

Границы можно применять к различным элементам документа, включая абзац, фрагмент текста внутри абзаца или ячейку таблицы.
## Методы

| Метод | Описание |
| --- | --- |
| [clearFormatting()](#clearFormatting--) | Сбрасывает свойства границы до значений по умолчанию. |
| [equals(Border rhs)](#equals-com.aspose.words.Border-) | Определяет, равна ли указанная граница по значению текущей границе. |
| [equals(Object obj)](#equals-java.lang.Object-) | Определяет, равен ли указанный объект по значению текущему объекту. |
| [getClass()](#getClass--) |  |
| [getColor()](#getColor--) | Получает цвет границы. |
| [getDistanceFromText()](#getDistanceFromText--) | Получает расстояние границы от текста или от края страницы в пунктах. |
| [getLineStyle()](#getLineStyle--) | Получает стиль границы. |
| [getLineWidth()](#getLineWidth--) | Получает ширину границы в пунктах. |
| [getShadow()](#getShadow--) | Получает значение, указывающее, есть ли у границы тень. |
| [hashCode()](#hashCode--) |  |
| [isInheritedComplexAttr()](#isInheritedComplexAttr--) |  |
| [isVisible()](#isVisible--) | Возвращает true, если LineStyle не является LineStyle.None. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setColor(Color value)](#setColor-java.awt.Color-) | Задает цвет границы. |
| [setDistanceFromText(double value)](#setDistanceFromText-double-) | Устанавливает расстояние границы от текста или от края страницы в пунктах. |
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


Сбрасывает свойства границы до значений по умолчанию. Когда свойства границы сбрасываются до значений по умолчанию, граница становится невидимой.

### equals(Border rhs) {#equals-com.aspose.words.Border-}
```
public boolean equals(Border rhs)
```


Определяет, равна ли указанная граница по значению текущей границе.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| rhs | [Border](../../com.aspose.words/border) |  |

**Возвращает:**
логический
### equals(Object obj) {#equals-java.lang.Object-}
```
public boolean equals(Object obj)
```


Определяет, равен ли указанный объект по значению текущему объекту.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Возвращает:**
логический
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

**Возвращает:**
java.awt.Color — цвет границы.
### getDistanceFromText() {#getDistanceFromText--}
```
public double getDistanceFromText()
```


Получает расстояние границы от текста или от края страницы в пунктах. Не имеет никакого эффекта и будет автоматически обнулен для границ ячеек таблицы.

**Возвращает:**
double - Расстояние границы от текста или от края страницы в пунктах.
### getLineStyle() {#getLineStyle--}
```
public int getLineStyle()
```


Получает стиль границы.

Если вы установите для стиля линии значение none, то ширина линии автоматически изменится на ноль.

**Возвращает:**
int - Стиль границы. Возвращаемое значение является одним из[LineStyle](../../com.aspose.words/linestyle) константы.
### getLineWidth() {#getLineWidth--}
```
public double getLineWidth()
```


Получает ширину границы в пунктах.

Если вы установите ширину линии больше нуля, когда стиль линии не задан, стиль линии автоматически изменится на одну линию.

**Возвращает:**
double - Ширина границы в пунктах.
### getShadow() {#getShadow--}
```
public boolean getShadow()
```


Получает значение, указывающее, есть ли у границы тень.

В Microsoft Word, чтобы граница имела тень, границы со всех четырех сторон (слева, сверху, справа и снизу) должны быть одного типа, ширины, цвета, и все они должны иметь свойство Shadow, установленное в true.

**Возвращает:**
boolean — значение, указывающее, есть ли у границы тень.
### hashCode() {#hashCode--}
```
public int hashCode()
```




**Возвращает:**
инт
### isInheritedComplexAttr() {#isInheritedComplexAttr--}
```
public boolean isInheritedComplexAttr()
```




**Возвращает:**
логический
### isVisible() {#isVisible--}
```
public boolean isVisible()
```


Возвращает true, если LineStyle не является LineStyle.None.

**Возвращает:**
boolean — Истинно, если LineStyle не LineStyle.None.
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

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.awt.Color | Цвет границы. |

### setDistanceFromText(double value) {#setDistanceFromText-double-}
```
public void setDistanceFromText(double value)
```


Устанавливает расстояние границы от текста или от края страницы в пунктах. Не имеет никакого эффекта и будет автоматически обнулен для границ ячеек таблицы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Расстояние границы от текста или от края страницы в пунктах. |

### setLineStyle(int value) {#setLineStyle-int-}
```
public void setLineStyle(int value)
```


Устанавливает стиль границы.

Если вы установите для стиля линии значение none, то ширина линии автоматически изменится на ноль.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Стиль границы. Значение должно быть одним из[LineStyle](../../com.aspose.words/linestyle) константы. |

### setLineWidth(double value) {#setLineWidth-double-}
```
public void setLineWidth(double value)
```


Устанавливает ширину границы в пунктах.

Если вы установите ширину линии больше нуля, когда стиль линии не задан, стиль линии автоматически изменится на одну линию.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Ширина границы в пунктах. |

### setShadow(boolean value) {#setShadow-boolean-}
```
public void setShadow(boolean value)
```


Задает значение, указывающее, есть ли у границы тень.

В Microsoft Word, чтобы граница имела тень, границы со всех четырех сторон (слева, сверху, справа и снизу) должны быть одного типа, ширины, цвета, и все они должны иметь свойство Shadow, установленное в true.

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
