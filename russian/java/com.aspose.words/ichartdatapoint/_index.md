---
title: IChartDataPoint
second_title: Справочник по API Aspose.Words для Java
description: Содержит свойства одной точки данных на диаграмме.
type: docs
weight: 633
url: /ru/java/com.aspose.words/ichartdatapoint/
---
```
public interface IChartDataPoint
```

Содержит свойства одной точки данных на диаграмме.
## Методы

| Метод | Описание |
| --- | --- |
| [getBubble3D()](#getBubble3D--) | Указывает, следует ли применять к пузырькам в пузырьковой диаграмме трехмерный эффект. |
| [getExplosion()](#getExplosion--) | Определяет величину, на которую точка данных должна быть перемещена от центра круговой диаграммы. |
| [getInvertIfNegative()](#getInvertIfNegative--) | Указывает, должен ли родительский элемент инвертировать свои цвета, если значение отрицательное. |
| [getMarker()](#getMarker--) | Указывает маркер данных. |
| [setBubble3D(boolean value)](#setBubble3D-boolean-) | Указывает, следует ли применять к пузырькам в пузырьковой диаграмме трехмерный эффект. |
| [setExplosion(int value)](#setExplosion-int-) | Определяет величину, на которую точка данных должна быть перемещена от центра круговой диаграммы. |
| [setInvertIfNegative(boolean value)](#setInvertIfNegative-boolean-) | Указывает, должен ли родительский элемент инвертировать свои цвета, если значение отрицательное. |
### getBubble3D() {#getBubble3D--}
```
public abstract boolean getBubble3D()
```


Указывает, следует ли применять к пузырькам в пузырьковой диаграмме трехмерный эффект.

**Возвращает:**
boolean - соответствующее логическое значение.
### getExplosion() {#getExplosion--}
```
public abstract int getExplosion()
```


Определяет величину, на которую точка данных должна быть перемещена от центра круговой диаграммы. Может быть отрицательным, отрицательное значение означает, что свойство не задано и не должно применяться разнесение. Применяется только к круговым диаграммам.

**Возвращает:**
int - соответствующее значение int.
### getInvertIfNegative() {#getInvertIfNegative--}
```
public abstract boolean getInvertIfNegative()
```


Указывает, должен ли родительский элемент инвертировать свои цвета, если значение отрицательное.

**Возвращает:**
boolean - соответствующее логическое значение.
### getMarker() {#getMarker--}
```
public abstract ChartMarker getMarker()
```


Указывает маркер данных. Маркер создается автоматически по запросу.

**Возвращает:**
[ChartMarker](../../com.aspose.words/chartmarker) - соответствующий[ChartMarker](../../com.aspose.words/chartmarker) ценность.
### setBubble3D(boolean value) {#setBubble3D-boolean-}
```
public abstract void setBubble3D(boolean value)
```


Указывает, следует ли применять к пузырькам в пузырьковой диаграмме трехмерный эффект.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setExplosion(int value) {#setExplosion-int-}
```
public abstract void setExplosion(int value)
```


Определяет величину, на которую точка данных должна быть перемещена от центра круговой диаграммы. Может быть отрицательным, отрицательное значение означает, что свойство не задано и не должно применяться разнесение. Применяется только к круговым диаграммам.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее целочисленное значение. |

### setInvertIfNegative(boolean value) {#setInvertIfNegative-boolean-}
```
public abstract void setInvertIfNegative(boolean value)
```


Указывает, должен ли родительский элемент инвертировать свои цвета, если значение отрицательное.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |
