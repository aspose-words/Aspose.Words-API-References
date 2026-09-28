---
title: "Aspose::Words::Drawing::Charts::ChartXValue класс"
linktitle: "ChartXValue"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::ChartXValue класс. Представляет значение X для серии диаграммы в C++."
type: docs
weight: 18200
url: /ru/cpp/aspose.words.drawing.charts/chartxvalue/
---
## ChartXValue class


Представляет значение X для серии диаграммы.

```cpp
class ChartXValue : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Возвращает флаг, указывающий, равен ли указанный объект текущему объекту значения X. |
| static [FromDateTime](./fromdatetime/)(System::DateTime) | Создает экземпляр [ChartXValue](./) типа [DateTime](../chartxvaluetype/). |
| static [FromDouble](./fromdouble/)(double) | Создает экземпляр [ChartXValue](./) типа [Double](../chartxvaluetype/). |
| static [FromMultilevelValue](./frommultilevelvalue/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartMultilevelValue\>\&) | Создает экземпляр [ChartXValue](./) типа [Multilevel](../chartxvaluetype/). |
| static [FromString](./fromstring/)(const System::String\&) | Создает экземпляр [ChartXValue](./) типа [String](../chartxvaluetype/). |
| static [FromTimeSpan](./fromtimespan/)(System::TimeSpan) | Создает экземпляр [ChartXValue](./) типа [Time](../chartxvaluetype/). |
| [get_DateTimeValue](./get_datetimevalue/)() const | Получает сохраненное значение datetime. |
| [get_DoubleValue](./get_doublevalue/)() const | Получает сохраненное числовое значение. |
| [get_MultilevelValue](./get_multilevelvalue/)() const | Получает сохраненное значение multilevel. |
| [get_StringValue](./get_stringvalue/)() const | Получает сохраненное строковое значение. |
| [get_TimeValue](./get_timevalue/)() const | Получает сохраненное значение времени. |
| [get_ValueType](./get_valuetype/)() const | Получает тип X‑значения, сохраненного в объекте. |
| [GetHashCode](./gethashcode/)() const override | Получает хеш‑код текущего объекта X‑значения. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Примечания


Этот класс содержит несколько статических методов для создания X‑значения определенного типа. Свойство [ValueType](./get_valuetype/) позволяет определить тип существующего X‑значения.

Все ненулевые X‑значения серии диаграммы должны быть одного типа [ChartXValueType](../chartxvaluetype/).

## Примеры



Показывает, как заполнять серии диаграммы данными.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = chart->get_Series()->idx_get(0);

// Очистить значения X и Y первой серии.
series1->ClearValues();

// Заполнить серию данными.
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10), 10);
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(5), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(5));
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(7), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(11));
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(9));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series2 = chart->get_Series()->idx_get(1);
// Очистить значения X и Y второй серии.
series2->Clear();

// Заполнить серию данными.
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(2), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(4));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(4), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(7));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(6), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(14));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(8), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(7));

doc->Save(get_ArtifactsDir() + u"Charts.PopulateChartWithData.docx");
```

## См. также

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
