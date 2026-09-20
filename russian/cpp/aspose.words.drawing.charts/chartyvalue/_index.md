---
title: "Aspose::Words::Drawing::Charts::ChartYValue класс"
linktitle: "ChartYValue"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::ChartYValue класс. Представляет значение Y для серии диаграммы в C++."
type: docs
weight: 18600
url: /ru/cpp/aspose.words.drawing.charts/chartyvalue/
---
## ChartYValue class


Представляет значение Y для серии диаграммы.

```cpp
class ChartYValue : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Возвращает флаг, указывающий, равен ли указанный объект текущему объекту значения Y. |
| static [FromDateTime](./fromdatetime/)(System::DateTime) | Создаёт экземпляр [ChartYValue](./) типа [DateTime](../chartyvaluetype/). |
| static [FromDouble](./fromdouble/)(double) | Создаёт экземпляр [ChartYValue](./) типа [Double](../chartyvaluetype/). |
| static [FromTimeSpan](./fromtimespan/)(System::TimeSpan) | Создаёт экземпляр [ChartYValue](./) типа [Time](../chartyvaluetype/). |
| [get_DateTimeValue](./get_datetimevalue/)() const | Получает сохраненное значение datetime. |
| [get_DoubleValue](./get_doublevalue/)() const | Получает сохраненное числовое значение. |
| [get_TimeValue](./get_timevalue/)() const | Получает сохраненное значение времени. |
| [get_ValueType](./get_valuetype/)() const | Возвращает тип значения Y, хранящегося в объекте. |
| [GetHashCode](./gethashcode/)() const override | Возвращает хеш-код текущего объекта значения Y. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Примечания


Этот класс содержит несколько статических методов для создания значения Y определённого типа. Свойство [ValueType](./get_valuetype/) позволяет определить тип существующего значения Y.

Все ненулевые значения Y серии диаграммы должны быть одного типа [ChartYValueType](../chartyvaluetype/).
## См. также

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
