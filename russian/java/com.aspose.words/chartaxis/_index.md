---
title: ChartAxis
second_title: Справочник по API Aspose.Words для Java
description: Представляет параметры оси диаграммы.
type: docs
weight: 56
url: /ru/java/com.aspose.words/chartaxis/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Cloneable
```
public class ChartAxis implements Cloneable
```

Представляет параметры оси диаграммы.

 Чтобы узнать больше, посетите**Working with Charts** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAxisBetweenCategories()](#getAxisBetweenCategories--) | Получает флаг, указывающий, пересекает ли ось значений ось категорий между категориями. |
| [getBaseTimeUnit()](#getBaseTimeUnit--) | Получает наименьшую единицу времени, представленную на оси категорий времени. |
| [getCategoryType()](#getCategoryType--) | Получает тип оси категорий. |
| [getClass()](#getClass--) |  |
| [getCrosses()](#getCrosses--) | Указывает, как эта ось пересекает перпендикулярную ось. |
| [getCrossesAt()](#getCrossesAt--) | Указывает, где на перпендикулярной оси ось пересекается. |
| [getDisplayUnit()](#getDisplayUnit--) | Указывает значение масштабирования отображаемых единиц для оси значений. |
| [getDocument()](#getDocument--) | Возвращает документ, принадлежащий правообладателю. |
| [getHidden()](#getHidden--) | Получает флаг, указывающий, скрыта эта ось или нет. |
| [getMajorTickMark()](#getMajorTickMark--) | Получает основные галочки. |
| [getMajorUnit()](#getMajorUnit--) | Получает расстояние между основными делениями. |
| [getMajorUnitIsAuto()](#getMajorUnitIsAuto--) | Получает флаг, указывающий, следует ли использовать расстояние по умолчанию между основными делениями. |
| [getMajorUnitScale()](#getMajorUnitScale--) | Получает значение шкалы для основных делений на оси категорий времени. |
| [getMinorTickMark()](#getMinorTickMark--) | Получает второстепенные деления для оси. |
| [getMinorUnit()](#getMinorUnit--) | Получает расстояние между второстепенными делениями. |
| [getMinorUnitIsAuto()](#getMinorUnitIsAuto--) | Получает флаг, указывающий, следует ли использовать расстояние по умолчанию между второстепенными делениями. |
| [getMinorUnitScale()](#getMinorUnitScale--) | Получает значение шкалы для второстепенных делений на оси категорий времени. |
| [getNumberFormat()](#getNumberFormat--) |  Возвращает[ChartNumberFormat](../../com.aspose.words/chartnumberformat) объект, который позволяет определять числовые форматы для оси. |
| [getReverseOrder()](#getReverseOrder--) | Получает флаг, указывающий, должны ли значения оси отображаться в обратном порядке, т.е. |
| [getScaling()](#getScaling--) | Предоставляет доступ к параметрам масштабирования оси. |
| [getTickLabelAlignment()](#getTickLabelAlignment--) | Получает выравнивание текста меток деления оси. |
| [getTickLabelOffset()](#getTickLabelOffset--) | Получает расстояние меток от оси. |
| [getTickLabelPosition()](#getTickLabelPosition--) | Получает положение меток деления на оси. |
| [getTickLabelSpacing()](#getTickLabelSpacing--) | Получает интервал, с которым отрисовываются метки делений. |
| [getTickLabelSpacingIsAuto()](#getTickLabelSpacingIsAuto--) | Получает флаг, указывающий, следует ли использовать автоматический интервал отрисовки тиковых меток. |
| [getTickMarkSpacing()](#getTickMarkSpacing--) | Получает интервал, с которым рисуются деления. |
| [getTitle()](#getTitle--) |  |
| [getTitleDeleted()](#getTitleDeleted--) |  |
| [getTitlePosition()](#getTitlePosition--) |  |
| [getType()](#getType--) | Возвращает тип оси. |
| [hashCode()](#hashCode--) |  |
| [isInherited()](#isInherited--) |  |
| [isVisible()](#isVisible--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setAxisBetweenCategories(boolean value)](#setAxisBetweenCategories-boolean-) | Устанавливает флаг, указывающий, пересекает ли ось значений ось категорий между категориями. |
| [setBaseTimeUnit(int value)](#setBaseTimeUnit-int-) | Задает наименьшую единицу времени, представленную на оси категорий времени. |
| [setCategoryType(int value)](#setCategoryType-int-) | Устанавливает тип оси категорий. |
| [setCrosses(int value)](#setCrosses-int-) | Указывает, как эта ось пересекает перпендикулярную ось. |
| [setCrossesAt(double value)](#setCrossesAt-double-) | Указывает, где на перпендикулярной оси ось пересекается. |
| [setHidden(boolean value)](#setHidden-boolean-) | Устанавливает флаг, указывающий, скрыта эта ось или нет. |
| [setMajorTickMark(int value)](#setMajorTickMark-int-) | Устанавливает основные деления. |
| [setMajorUnit(double value)](#setMajorUnit-double-) | Устанавливает расстояние между основными делениями. |
| [setMajorUnitIsAuto(boolean value)](#setMajorUnitIsAuto-boolean-) | Устанавливает флаг, указывающий, следует ли использовать расстояние по умолчанию между основными делениями. |
| [setMajorUnitScale(int value)](#setMajorUnitScale-int-) | Задает значение шкалы для основных делений на оси категорий времени. |
| [setMinorTickMark(int value)](#setMinorTickMark-int-) | Устанавливает второстепенные деления для оси. |
| [setMinorUnit(double value)](#setMinorUnit-double-) | Устанавливает расстояние между второстепенными делениями. |
| [setMinorUnitIsAuto(boolean value)](#setMinorUnitIsAuto-boolean-) | Устанавливает флаг, указывающий, следует ли использовать расстояние по умолчанию между второстепенными делениями. |
| [setMinorUnitScale(int value)](#setMinorUnitScale-int-) | Устанавливает значение масштаба для второстепенных делений на оси категорий времени. |
| [setReverseOrder(boolean value)](#setReverseOrder-boolean-) | Устанавливает флаг, указывающий, должны ли значения оси отображаться в обратном порядке, т.е. |
| [setTickLabelAlignment(int value)](#setTickLabelAlignment-int-) | Устанавливает выравнивание текста меток деления оси. |
| [setTickLabelOffset(int value)](#setTickLabelOffset-int-) | Устанавливает расстояние меток от оси. |
| [setTickLabelPosition(int value)](#setTickLabelPosition-int-) | Задает положение галочек на оси. |
| [setTickLabelSpacing(int value)](#setTickLabelSpacing-int-) | Устанавливает интервал, с которым рисуются галочки. |
| [setTickLabelSpacingIsAuto(boolean value)](#setTickLabelSpacingIsAuto-boolean-) | Устанавливает флаг, указывающий, следует ли использовать автоматический интервал отрисовки тиковых меток. |
| [setTickMarkSpacing(int value)](#setTickMarkSpacing-int-) | Устанавливает интервал, с которым рисуются деления. |
| [setTitle(ChartTitle value)](#setTitle-com.aspose.words.ChartTitle-) |  |
| [setTitleDeleted(boolean value)](#setTitleDeleted-boolean-) |  |
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
### getAxisBetweenCategories() {#getAxisBetweenCategories--}
```
public boolean getAxisBetweenCategories()
```


Получает флаг, указывающий, пересекает ли ось значений ось категорий между категориями. Свойство действует только для осей значений. Он не поддерживается новыми диаграммами MS Office 2016.

**Возвращает:**
boolean — Флаг, указывающий, пересекает ли ось значений ось категорий между категориями.
### getBaseTimeUnit() {#getBaseTimeUnit--}
```
public int getBaseTimeUnit()
```


Получает наименьшую единицу времени, представленную на оси категорий времени. Свойство действует только для осей категорий времени.

**Возвращает:**
 int — наименьшая единица измерения времени, представленная на оси категории времени. Возвращаемое значение является одним из[AxisTimeUnit](../../com.aspose.words/axistimeunit) константы.
### getCategoryType() {#getCategoryType--}
```
public int getCategoryType()
```


 Получает тип оси категорий. Только текстовые категории ([AxisCategoryType.CATEGORY](../../com.aspose.words/axiscategorytype\#CATEGORY)) разрешены в новых диаграммах MS Office 2016.

**Возвращает:**
 int - Тип оси категорий. Возвращаемое значение является одним из[AxisCategoryType](../../com.aspose.words/axiscategorytype) константы.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getCrosses() {#getCrosses--}
```
public int getCrosses()
```


Указывает, как эта ось пересекает перпендикулярную ось.

 Значение по умолчанию[AxisCrosses.AUTOMATIC](../../com.aspose.words/axiscrosses\#AUTOMATIC).

Это свойство не поддерживается новыми диаграммами MS Office 2016.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[AxisCrosses](../../com.aspose.words/axiscrosses) константы.
### getCrossesAt() {#getCrossesAt--}
```
public double getCrossesAt()
```


Указывает, где на перпендикулярной оси ось пересекается.

Свойство имеет силу, только если[getCrosses()](../../com.aspose.words/chartaxis\#getCrosses--) / [setCrosses(int)](../../com.aspose.words/chartaxis\#setCrosses-int-) настроены на[AxisCrosses.CUSTOM](../../com.aspose.words/axiscrosses\#CUSTOM). Он не поддерживается новыми диаграммами MS Office 2016.

Единицы определяются типом оси. Если ось является осью значений, значением свойства является десятичное число на оси значений. Если ось представляет собой ось категории времени, значение определяется как целое число дней относительно базовой даты (30/12/1899). Для оси текстовых категорий значение представляет собой целочисленный номер категории, начиная с 1 в качестве первой категории.

**Возвращает:**
double - соответствующее двойное значение.
### getDisplayUnit() {#getDisplayUnit--}
```
public AxisDisplayUnit getDisplayUnit()
```


Указывает значение масштабирования отображаемых единиц для оси значений. Свойство действует только для осей значений.

**Возвращает:**
[AxisDisplayUnit](../../com.aspose.words/axisdisplayunit) - соответствующий[AxisDisplayUnit](../../com.aspose.words/axisdisplayunit) ценность.
### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


Возвращает документ, принадлежащий правообладателю.

**Возвращает:**
[DocumentBase](../../com.aspose.words/documentbase) - Документ, принадлежащий правообладателю.
### getHidden() {#getHidden--}
```
public boolean getHidden()
```


 Получает флаг, указывающий, скрыта эта ось или нет. Значение по умолчанию**false**.

**Возвращает:**
boolean - Флаг, указывающий, скрыта эта ось или нет.
### getMajorTickMark() {#getMajorTickMark--}
```
public int getMajorTickMark()
```


Получает основные галочки.

**Возвращает:**
 int - основные метки деления. Возвращаемое значение является одним из[AxisTickMark](../../com.aspose.words/axistickmark) константы.
### getMajorUnit() {#getMajorUnit--}
```
public double getMajorUnit()
```


Получает расстояние между основными делениями.

Допустимый диапазон значения больше нуля. Свойство влияет на категорию времени и оси значений.

 Установка этого свойства устанавливает[getMajorUnitIsAuto()](../../com.aspose.words/chartaxis\#getMajorUnitIsAuto--) / [setMajorUnitIsAuto(boolean)](../../com.aspose.words/chartaxis\#setMajorUnitIsAuto-boolean-) собственность на**false**.

**Возвращает:**
double - Расстояние между основными делениями.
### getMajorUnitIsAuto() {#getMajorUnitIsAuto--}
```
public boolean getMajorUnitIsAuto()
```


Получает флаг, указывающий, следует ли использовать расстояние по умолчанию между основными делениями. Свойство влияет на категорию времени и оси значений.

**Возвращает:**
boolean - Флаг, указывающий, должно ли использоваться расстояние по умолчанию между основными делениями.
### getMajorUnitScale() {#getMajorUnitScale--}
```
public int getMajorUnitScale()
```


Получает значение шкалы для основных делений на оси категорий времени. Свойство действует только для осей категории времени.

**Возвращает:**
 int — значение шкалы для основных отметок на оси категорий времени. Возвращаемое значение является одним из[AxisTimeUnit](../../com.aspose.words/axistimeunit) константы.
### getMinorTickMark() {#getMinorTickMark--}
```
public int getMinorTickMark()
```


Получает второстепенные деления для оси.

**Возвращает:**
 int — второстепенные деления для оси. Возвращаемое значение является одним из[AxisTickMark](../../com.aspose.words/axistickmark) константы.
### getMinorUnit() {#getMinorUnit--}
```
public double getMinorUnit()
```


Получает расстояние между второстепенными делениями.

Допустимый диапазон значения больше нуля. Свойство влияет на категорию времени и оси значений.

 Установка этого свойства устанавливает[getMinorUnitIsAuto()](../../com.aspose.words/chartaxis\#getMinorUnitIsAuto--) / [setMinorUnitIsAuto(boolean)](../../com.aspose.words/chartaxis\#setMinorUnitIsAuto-boolean-) собственность на**false**.

**Возвращает:**
double - Расстояние между второстепенными делениями.
### getMinorUnitIsAuto() {#getMinorUnitIsAuto--}
```
public boolean getMinorUnitIsAuto()
```


Получает флаг, указывающий, следует ли использовать расстояние по умолчанию между второстепенными делениями. Свойство влияет на категорию времени и оси значений.

**Возвращает:**
boolean - Флаг, указывающий, должно ли использоваться расстояние по умолчанию между второстепенными делениями.
### getMinorUnitScale() {#getMinorUnitScale--}
```
public int getMinorUnitScale()
```


Получает значение шкалы для второстепенных делений на оси категорий времени. Свойство действует только для осей категорий времени.

**Возвращает:**
 int — значение масштаба для второстепенных делений на оси категории времени. Возвращаемое значение является одним из[AxisTimeUnit](../../com.aspose.words/axistimeunit) константы.
### getNumberFormat() {#getNumberFormat--}
```
public ChartNumberFormat getNumberFormat()
```


 Возвращает[ChartNumberFormat](../../com.aspose.words/chartnumberformat) объект, который позволяет определять числовые форматы для оси.

**Возвращает:**
[ChartNumberFormat](../../com.aspose.words/chartnumberformat) - А[ChartNumberFormat](../../com.aspose.words/chartnumberformat) объект, который позволяет определять числовые форматы для оси.
### getReverseOrder() {#getReverseOrder--}
```
public boolean getReverseOrder()
```


 Получает флаг, указывающий, должны ли значения оси отображаться в обратном порядке, т.е. от максимального к минимальному. Это свойство не поддерживается новыми диаграммами MS Office 2016. Значение по умолчанию**false**.

**Возвращает:**
boolean - Флаг, указывающий, должны ли значения оси отображаться в обратном порядке, т.е.
### getScaling() {#getScaling--}
```
public AxisScaling getScaling()
```


Предоставляет доступ к параметрам масштабирования оси.

**Возвращает:**
[AxisScaling](../../com.aspose.words/axisscaling) - соответствующий[AxisScaling](../../com.aspose.words/axisscaling) ценность.
### getTickLabelAlignment() {#getTickLabelAlignment--}
```
public int getTickLabelAlignment()
```


Получает выравнивание текста меток деления оси.

Это свойство действует только для многострочных меток.

 Значение по умолчанию[ParagraphAlignment.CENTER](../../com.aspose.words/paragraphalignment\#CENTER).

.

**Возвращает:**
 int - Выравнивание текста меток деления оси. Возвращаемое значение является одним из[ParagraphAlignment](../../com.aspose.words/paragraphalignment) константы.
### getTickLabelOffset() {#getTickLabelOffset--}
```
public int getTickLabelOffset()
```


Получает расстояние меток от оси.

Свойство представляет собой процент смещения метки по умолчанию.

Допустимый диапазон: от 0 до 1000 процентов включительно. Значение по умолчанию — 100%.

Свойство действует только для осей категорий. Он не поддерживается новыми диаграммами MS Office 2016.

**Возвращает:**
int - Расстояние меток от оси.
### getTickLabelPosition() {#getTickLabelPosition--}
```
public int getTickLabelPosition()
```


Получает положение меток деления на оси. Это свойство не поддерживается новыми диаграммами MS Office 2016.

**Возвращает:**
 int - Положение галочки на оси. Возвращаемое значение является одним из[AxisTickLabelPosition](../../com.aspose.words/axisticklabelposition) константы.
### getTickLabelSpacing() {#getTickLabelSpacing--}
```
public int getTickLabelSpacing()
```


Получает интервал, с которым отрисовываются метки делений.

Свойство действует для текстовых категорий и осей серий. Он не поддерживается новыми диаграммами MS Office 2016. Допустимый диапазон значения больше или равен 1.

 Установка этого свойства устанавливает[getTickLabelSpacingIsAuto()](../../com.aspose.words/chartaxis\#getTickLabelSpacingIsAuto--) / [setTickLabelSpacingIsAuto(boolean)](../../com.aspose.words/chartaxis\#setTickLabelSpacingIsAuto-boolean-) собственность на**false**.

**Возвращает:**
int - Интервал, с которым отрисовываются галочки.
### getTickLabelSpacingIsAuto() {#getTickLabelSpacingIsAuto--}
```
public boolean getTickLabelSpacingIsAuto()
```


Получает флаг, указывающий, следует ли использовать автоматический интервал отрисовки тиковых меток.

 Значение по умолчанию**true**.

Свойство действует для текстовых категорий и осей серий. Он не поддерживается новыми диаграммами MS Office 2016.

**Возвращает:**
boolean - Флаг, указывающий, следует ли использовать автоматический интервал отрисовки тиковых меток.
### getTickMarkSpacing() {#getTickMarkSpacing--}
```
public int getTickMarkSpacing()
```


Получает интервал, с которым рисуются деления.

Свойство действует для текстовых категорий и осей серий. Он не поддерживается новыми диаграммами MS Office 2016.

Допустимый диапазон значения больше или равен 1.

**Возвращает:**
int - Интервал, с которым рисуются деления.
### getTitle() {#getTitle--}
```
public ChartTitle getTitle()
```




**Возвращает:**
[ChartTitle](../../com.aspose.words/charttitle)
### getTitleDeleted() {#getTitleDeleted--}
```
public boolean getTitleDeleted()
```




**Возвращает:**
логический
### getTitlePosition() {#getTitlePosition--}
```
public int getTitlePosition()
```




**Возвращает:**
инт
### getType() {#getType--}
```
public int getType()
```


Возвращает тип оси.

**Возвращает:**
 int - Тип оси. Возвращаемое значение является одним из[ChartAxisType](../../com.aspose.words/chartaxistype) константы.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### isInherited() {#isInherited--}
```
public boolean isInherited()
```




**Возвращает:**
логический
### isVisible() {#isVisible--}
```
public boolean isVisible()
```




**Возвращает:**
логический
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setAxisBetweenCategories(boolean value) {#setAxisBetweenCategories-boolean-}
```
public void setAxisBetweenCategories(boolean value)
```


Устанавливает флаг, указывающий, пересекает ли ось значений ось категорий между категориями. Свойство действует только для осей значений. Он не поддерживается новыми диаграммами MS Office 2016.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Флаг, указывающий, пересекает ли ось значений ось категорий между категориями. |

### setBaseTimeUnit(int value) {#setBaseTimeUnit-int-}
```
public void setBaseTimeUnit(int value)
```


Задает наименьшую единицу времени, представленную на оси категории времени. Свойство действует только для осей категории времени.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Наименьшая единица времени, представленная на оси категории времени. Значение должно быть одним из[AxisTimeUnit](../../com.aspose.words/axistimeunit) константы. |

### setCategoryType(int value) {#setCategoryType-int-}
```
public void setCategoryType(int value)
```


 Устанавливает тип оси категорий. Только текстовые категории ([AxisCategoryType.CATEGORY](../../com.aspose.words/axiscategorytype\#CATEGORY)) разрешены в новых диаграммах MS Office 2016.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Тип оси категорий. Значение должно быть одним из[AxisCategoryType](../../com.aspose.words/axiscategorytype) константы. |

### setCrosses(int value) {#setCrosses-int-}
```
public void setCrosses(int value)
```


Указывает, как эта ось пересекает перпендикулярную ось.

 Значение по умолчанию[AxisCrosses.AUTOMATIC](../../com.aspose.words/axiscrosses\#AUTOMATIC).

Это свойство не поддерживается новыми диаграммами MS Office 2016.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[AxisCrosses](../../com.aspose.words/axiscrosses) константы. |

### setCrossesAt(double value) {#setCrossesAt-double-}
```
public void setCrossesAt(double value)
```


Указывает, где на перпендикулярной оси ось пересекается.

Свойство имеет силу, только если[getCrosses()](../../com.aspose.words/chartaxis\#getCrosses--) / [setCrosses(int)](../../com.aspose.words/chartaxis\#setCrosses-int-) настроены на[AxisCrosses.CUSTOM](../../com.aspose.words/axiscrosses\#CUSTOM). Он не поддерживается новыми диаграммами MS Office 2016.

Единицы определяются типом оси. Если ось является осью значений, значением свойства является десятичное число на оси значений. Если ось представляет собой ось категории времени, значение определяется как целое число дней относительно базовой даты (30/12/1899). Для оси текстовых категорий значение представляет собой целочисленный номер категории, начиная с 1 в качестве первой категории.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Соответствующее двойное значение. |

### setHidden(boolean value) {#setHidden-boolean-}
```
public void setHidden(boolean value)
```


 Устанавливает флаг, указывающий, скрыта эта ось или нет. Значение по умолчанию**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Флаг, указывающий, скрыта эта ось или нет. |

### setMajorTickMark(int value) {#setMajorTickMark-int-}
```
public void setMajorTickMark(int value)
```


Устанавливает основные деления.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Основные галочки. Значение должно быть одним из[AxisTickMark](../../com.aspose.words/axistickmark) константы. |

### setMajorUnit(double value) {#setMajorUnit-double-}
```
public void setMajorUnit(double value)
```


Устанавливает расстояние между основными делениями.

Допустимый диапазон значения больше нуля. Свойство влияет на категорию времени и оси значений.

 Установка этого свойства устанавливает[getMajorUnitIsAuto()](../../com.aspose.words/chartaxis\#getMajorUnitIsAuto--) / [setMajorUnitIsAuto(boolean)](../../com.aspose.words/chartaxis\#setMajorUnitIsAuto-boolean-) собственность на**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Расстояние между основными делениями. |

### setMajorUnitIsAuto(boolean value) {#setMajorUnitIsAuto-boolean-}
```
public void setMajorUnitIsAuto(boolean value)
```


Устанавливает флаг, указывающий, следует ли использовать расстояние по умолчанию между основными делениями. Свойство влияет на категорию времени и оси значений.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Флаг, указывающий, следует ли использовать расстояние по умолчанию между основными делениями. |

### setMajorUnitScale(int value) {#setMajorUnitScale-int-}
```
public void setMajorUnitScale(int value)
```


Задает значение шкалы для основных делений на оси категорий времени. Свойство действует только для осей категории времени.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Значение шкалы для основных делений на оси категорий времени. Значение должно быть одним из[AxisTimeUnit](../../com.aspose.words/axistimeunit) константы. |

### setMinorTickMark(int value) {#setMinorTickMark-int-}
```
public void setMinorTickMark(int value)
```


Устанавливает второстепенные деления для оси.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Второстепенные деления для оси. Значение должно быть одним из[AxisTickMark](../../com.aspose.words/axistickmark) константы. |

### setMinorUnit(double value) {#setMinorUnit-double-}
```
public void setMinorUnit(double value)
```


Устанавливает расстояние между второстепенными делениями.

Допустимый диапазон значения больше нуля. Свойство влияет на категорию времени и оси значений.

 Установка этого свойства устанавливает[getMinorUnitIsAuto()](../../com.aspose.words/chartaxis\#getMinorUnitIsAuto--) / [setMinorUnitIsAuto(boolean)](../../com.aspose.words/chartaxis\#setMinorUnitIsAuto-boolean-) собственность на**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Расстояние между второстепенными делениями. |

### setMinorUnitIsAuto(boolean value) {#setMinorUnitIsAuto-boolean-}
```
public void setMinorUnitIsAuto(boolean value)
```


Устанавливает флаг, указывающий, следует ли использовать расстояние по умолчанию между второстепенными делениями. Свойство влияет на категорию времени и оси значений.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Флаг, указывающий, следует ли использовать расстояние по умолчанию между второстепенными делениями. |

### setMinorUnitScale(int value) {#setMinorUnitScale-int-}
```
public void setMinorUnitScale(int value)
```


Устанавливает значение масштаба для второстепенных делений на оси категории времени. Свойство действует только для осей категории времени.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Значение масштаба для второстепенных делений на оси категории времени. Значение должно быть одним из[AxisTimeUnit](../../com.aspose.words/axistimeunit) константы. |

### setReverseOrder(boolean value) {#setReverseOrder-boolean-}
```
public void setReverseOrder(boolean value)
```


 Устанавливает флаг, указывающий, должны ли значения оси отображаться в обратном порядке, т.е. от максимального к минимальному. Это свойство не поддерживается новыми диаграммами MS Office 2016. Значение по умолчанию**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Флаг, указывающий, должны ли значения оси отображаться в обратном порядке, т.е. |

### setTickLabelAlignment(int value) {#setTickLabelAlignment-int-}
```
public void setTickLabelAlignment(int value)
```


Устанавливает выравнивание текста меток деления оси.

Это свойство действует только для многострочных меток.

 Значение по умолчанию[ParagraphAlignment.CENTER](../../com.aspose.words/paragraphalignment\#CENTER).

.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Выравнивание текста меток деления оси. Значение должно быть одним из[ParagraphAlignment](../../com.aspose.words/paragraphalignment) константы. |

### setTickLabelOffset(int value) {#setTickLabelOffset-int-}
```
public void setTickLabelOffset(int value)
```


Устанавливает расстояние меток от оси.

Свойство представляет собой процент смещения метки по умолчанию.

Допустимый диапазон: от 0 до 1000 процентов включительно. Значение по умолчанию — 100%.

Свойство действует только для осей категорий. Он не поддерживается новыми диаграммами MS Office 2016.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Расстояние меток от оси. |

### setTickLabelPosition(int value) {#setTickLabelPosition-int-}
```
public void setTickLabelPosition(int value)
```


Задает положение галочек на оси. Это свойство не поддерживается новыми диаграммами MS Office 2016.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Положение галочек на оси. Значение должно быть одним из[AxisTickLabelPosition](../../com.aspose.words/axisticklabelposition) константы. |

### setTickLabelSpacing(int value) {#setTickLabelSpacing-int-}
```
public void setTickLabelSpacing(int value)
```


Устанавливает интервал, с которым рисуются галочки.

Свойство действует для текстовых категорий и осей серий. Он не поддерживается новыми диаграммами MS Office 2016. Допустимый диапазон значения больше или равен 1.

 Установка этого свойства устанавливает[getTickLabelSpacingIsAuto()](../../com.aspose.words/chartaxis\#getTickLabelSpacingIsAuto--) / [setTickLabelSpacingIsAuto(boolean)](../../com.aspose.words/chartaxis\#setTickLabelSpacingIsAuto-boolean-) собственность на**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Интервал, с которым отрисовываются галочки. |

### setTickLabelSpacingIsAuto(boolean value) {#setTickLabelSpacingIsAuto-boolean-}
```
public void setTickLabelSpacingIsAuto(boolean value)
```


Устанавливает флаг, указывающий, следует ли использовать автоматический интервал отрисовки тиковых меток.

 Значение по умолчанию**true**.

Свойство действует для текстовых категорий и осей серий. Он не поддерживается новыми диаграммами MS Office 2016.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Флаг, указывающий, следует ли использовать автоматический интервал отрисовки тиковых меток. |

### setTickMarkSpacing(int value) {#setTickMarkSpacing-int-}
```
public void setTickMarkSpacing(int value)
```


Устанавливает интервал, с которым рисуются деления.

Свойство действует для текстовых категорий и осей серий. Он не поддерживается новыми диаграммами MS Office 2016.

Допустимый диапазон значения больше или равен 1.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Интервал, с которым рисуются деления. |

### setTitle(ChartTitle value) {#setTitle-com.aspose.words.ChartTitle-}
```
public void setTitle(ChartTitle value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [ChartTitle](../../com.aspose.words/charttitle) |  |

### setTitleDeleted(boolean value) {#setTitleDeleted-boolean-}
```
public void setTitleDeleted(boolean value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean |  |

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
