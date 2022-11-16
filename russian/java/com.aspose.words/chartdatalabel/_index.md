---
title: ChartDataLabel
second_title: Справочник по API Aspose.Words для Java
description: Представляет метку данных в точке диаграммы или на линии тренда.
type: docs
weight: 58
url: /ru/java/com.aspose.words/chartdatalabel/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Cloneable
```
public class ChartDataLabel implements Cloneable
```

Представляет метку данных в точке диаграммы или на линии тренда.

 Чтобы узнать больше, посетите**Working with Charts** документальная статья.

 В сериале,[ChartDataLabel](../../com.aspose.words/chartdatalabel) объект является членом[ChartDataLabelCollection](../../com.aspose.words/chartdatalabelcollection) .[ChartDataLabelCollection](../../com.aspose.words/chartdatalabelcollection) содержит[ChartDataLabel](../../com.aspose.words/chartdatalabel) объект для каждой точки.
## Методы

| Метод | Описание |
| --- | --- |
| [clearFormat()](#clearFormat--) | Очищает формат этой метки данных. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getIndex()](#getIndex--) | Указывает индекс содержащего элемента. |
| [getNumberFormat()](#getNumberFormat--) | Возвращает числовой формат родительского элемента. |
| [getSeparator()](#getSeparator--) | Получает разделитель строк, используемый для меток данных на диаграмме. |
| [getShowBubbleSize()](#getShowBubbleSize--) | Позволяет указать, должен ли отображаться размер пузырьков для меток данных на диаграмме. |
| [getShowCategoryName()](#getShowCategoryName--) | Позволяет указать, должно ли отображаться имя категории для меток данных на диаграмме. |
| [getShowDataLabelsRange()](#getShowDataLabelsRange--) | Позволяет указать, будут ли значения из диапазона меток данных отображаться в метках данных. |
| [getShowLeaderLines()](#getShowLeaderLines--) | Позволяет указать, нужно ли отображать линии выноски меток данных. |
| [getShowLegendKey()](#getShowLegendKey--) | Позволяет указать, должен ли отображаться ключ легенды для меток данных на диаграмме. |
| [getShowPercentage()](#getShowPercentage--) | Позволяет указать, должно ли процентное значение отображаться для меток данных на диаграмме. |
| [getShowSeriesName()](#getShowSeriesName--) | Получает логическое значение, указывающее поведение отображения имени ряда для меток данных на диаграмме. |
| [getShowValue()](#getShowValue--) | Позволяет указать, должны ли значения отображаться в метках данных. |
| [hashCode()](#hashCode--) |  |
| [isHidden()](#isHidden--) | Получает/устанавливает флаг, указывающий, скрыта ли эта метка. |
| [isHidden(boolean value)](#isHidden-boolean-) | Получает/устанавливает флаг, указывающий, скрыта ли эта метка. |
| [isInherited()](#isInherited--) |  |
| [isVisible()](#isVisible--) | Возвращает true, если у этой метки данных есть что отображать. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setSeparator(String value)](#setSeparator-java.lang.String-) | Задает разделитель строк, используемый для меток данных на диаграмме. |
| [setShowBubbleSize(boolean value)](#setShowBubbleSize-boolean-) | Позволяет указать, должен ли отображаться размер пузырьков для меток данных на диаграмме. |
| [setShowCategoryName(boolean value)](#setShowCategoryName-boolean-) | Позволяет указать, должно ли отображаться имя категории для меток данных на диаграмме. |
| [setShowDataLabelsRange(boolean value)](#setShowDataLabelsRange-boolean-) | Позволяет указать, будут ли значения из диапазона меток данных отображаться в метках данных. |
| [setShowLeaderLines(boolean value)](#setShowLeaderLines-boolean-) | Позволяет указать, нужно ли отображать линии выноски меток данных. |
| [setShowLegendKey(boolean value)](#setShowLegendKey-boolean-) | Позволяет указать, должен ли отображаться ключ легенды для меток данных на диаграмме. |
| [setShowPercentage(boolean value)](#setShowPercentage-boolean-) | Позволяет указать, должно ли процентное значение отображаться для меток данных на диаграмме. |
| [setShowSeriesName(boolean value)](#setShowSeriesName-boolean-) | Задает логическое значение, указывающее поведение отображения имени ряда для меток данных на диаграмме. |
| [setShowValue(boolean value)](#setShowValue-boolean-) | Позволяет указать, должны ли значения отображаться в метках данных. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clearFormat() {#clearFormat--}
```
public void clearFormat()
```


Очищает формат этой метки данных. Для свойств устанавливаются значения по умолчанию, определенные в родительской коллекции меток данных.

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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getIndex() {#getIndex--}
```
public int getIndex()
```


Указывает индекс содержащего элемента. Этот индекс должен определять, к какой из дочерних коллекций родителя относится этот элемент. Значение по умолчанию — 0.

**Возвращает:**
int - соответствующее значение int.
### getNumberFormat() {#getNumberFormat--}
```
public ChartNumberFormat getNumberFormat()
```


Возвращает числовой формат родительского элемента.

**Возвращает:**
[ChartNumberFormat](../../com.aspose.words/chartnumberformat) - Числовой формат родительского элемента.
### getSeparator() {#getSeparator--}
```
public String getSeparator()
```


Получает разделитель строк, используемый для меток данных на диаграмме. По умолчанию используется запятая, за исключением круговых диаграмм, показывающих только название категории и процентное соотношение, когда вместо этого следует использовать разрыв строки.

**Возвращает:**
java.lang.String — разделитель строк, используемый для меток данных на диаграмме.
### getShowBubbleSize() {#getShowBubbleSize--}
```
public boolean getShowBubbleSize()
```


Позволяет указать, должен ли отображаться размер пузырьков для меток данных на диаграмме. Применяется только к пузырьковым диаграммам. Значение по умолчанию — ложь.

**Возвращает:**
boolean - соответствующее логическое значение.
### getShowCategoryName() {#getShowCategoryName--}
```
public boolean getShowCategoryName()
```


Позволяет указать, должно ли отображаться имя категории для меток данных на диаграмме. Значение по умолчанию — ложь.

**Возвращает:**
boolean - соответствующее логическое значение.
### getShowDataLabelsRange() {#getShowDataLabelsRange--}
```
public boolean getShowDataLabelsRange()
```


Позволяет указать, будут ли значения из диапазона меток данных отображаться в метках данных. Значение по умолчанию — ложь.

**Возвращает:**
boolean - соответствующее логическое значение.
### getShowLeaderLines() {#getShowLeaderLines--}
```
public boolean getShowLeaderLines()
```


Позволяет указать, нужно ли отображать линии выноски меток данных. Значение по умолчанию — ложь. Применяется только к круговым диаграммам. Линии выноски создают визуальную связь между меткой данных и соответствующей точкой данных.

**Возвращает:**
boolean - соответствующее логическое значение.
### getShowLegendKey() {#getShowLegendKey--}
```
public boolean getShowLegendKey()
```


Позволяет указать, должен ли отображаться ключ легенды для меток данных на диаграмме. Значение по умолчанию — ложь.

**Возвращает:**
boolean - соответствующее логическое значение.
### getShowPercentage() {#getShowPercentage--}
```
public boolean getShowPercentage()
```


Позволяет указать, должно ли процентное значение отображаться для меток данных на диаграмме. Значение по умолчанию — ложь.

**Возвращает:**
boolean - соответствующее логическое значение.
### getShowSeriesName() {#getShowSeriesName--}
```
public boolean getShowSeriesName()
```


Получает логическое значение, указывающее поведение отображения имени ряда для меток данных на диаграмме. Значение true, чтобы показать название серии. Ложь скрывать. По умолчанию ложь.

**Возвращает:**
boolean — логическое значение, указывающее поведение отображения имени ряда для меток данных на диаграмме.
### getShowValue() {#getShowValue--}
```
public boolean getShowValue()
```


Позволяет указать, должны ли значения отображаться в метках данных. Значение по умолчанию — ложь.

**Возвращает:**
boolean - соответствующее логическое значение.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### isHidden() {#isHidden--}
```
public boolean isHidden()
```


 Получает/устанавливает флаг, указывающий, скрыта ли эта метка. Значение по умолчанию**false**.

**Возвращает:**
boolean - соответствующее логическое значение.
### isHidden(boolean value) {#isHidden-boolean-}
```
public void isHidden(boolean value)
```


 Получает/устанавливает флаг, указывающий, скрыта ли эта метка. Значение по умолчанию**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

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


Возвращает true, если у этой метки данных есть что отображать.

**Возвращает:**
boolean — Истинно, если эта метка данных что-то отображает.
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setSeparator(String value) {#setSeparator-java.lang.String-}
```
public void setSeparator(String value)
```


Задает разделитель строк, используемый для меток данных на диаграмме. По умолчанию используется запятая, за исключением круговых диаграмм, показывающих только название категории и процентное соотношение, когда вместо этого следует использовать разрыв строки.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Разделитель строк, используемый для меток данных на диаграмме. |

### setShowBubbleSize(boolean value) {#setShowBubbleSize-boolean-}
```
public void setShowBubbleSize(boolean value)
```


Позволяет указать, должен ли отображаться размер пузырьков для меток данных на диаграмме. Применяется только к пузырьковым диаграммам. Значение по умолчанию — ложь.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setShowCategoryName(boolean value) {#setShowCategoryName-boolean-}
```
public void setShowCategoryName(boolean value)
```


Позволяет указать, должно ли отображаться имя категории для меток данных на диаграмме. Значение по умолчанию — ложь.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setShowDataLabelsRange(boolean value) {#setShowDataLabelsRange-boolean-}
```
public void setShowDataLabelsRange(boolean value)
```


Позволяет указать, будут ли значения из диапазона меток данных отображаться в метках данных. Значение по умолчанию — ложь.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setShowLeaderLines(boolean value) {#setShowLeaderLines-boolean-}
```
public void setShowLeaderLines(boolean value)
```


Позволяет указать, нужно ли отображать линии выноски меток данных. Значение по умолчанию — ложь. Применяется только к круговым диаграммам. Линии выноски создают визуальную связь между меткой данных и соответствующей точкой данных.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setShowLegendKey(boolean value) {#setShowLegendKey-boolean-}
```
public void setShowLegendKey(boolean value)
```


Позволяет указать, должен ли отображаться ключ легенды для меток данных на диаграмме. Значение по умолчанию — ложь.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setShowPercentage(boolean value) {#setShowPercentage-boolean-}
```
public void setShowPercentage(boolean value)
```


Позволяет указать, должно ли процентное значение отображаться для меток данных на диаграмме. Значение по умолчанию — ложь.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setShowSeriesName(boolean value) {#setShowSeriesName-boolean-}
```
public void setShowSeriesName(boolean value)
```


Задает логическое значение, указывающее поведение отображения имени ряда для меток данных на диаграмме. Значение true, чтобы показать название серии. Ложь скрывать. По умолчанию ложь.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Логическое значение, указывающее поведение отображения имени ряда для меток данных на диаграмме. |

### setShowValue(boolean value) {#setShowValue-boolean-}
```
public void setShowValue(boolean value)
```


Позволяет указать, должны ли значения отображаться в метках данных. Значение по умолчанию — ложь.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

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
