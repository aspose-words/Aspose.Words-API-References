---
title: "Класс Aspose::Words::Drawing::Charts::ChartXValueCollection"
linktitle: "ChartXValueCollection"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Drawing::Charts::ChartXValueCollection. Представляет коллекцию значений X для ряда диаграммы в C++."
type: docs
weight: 18400
url: /ru/cpp/aspose.words.drawing.charts/chartxvaluecollection/
---
## ChartXValueCollection class


Представляет коллекцию значений X для серии диаграммы.

```cpp
class ChartXValueCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValue>>
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Count](./get_count/)() | Возвращает количество элементов в этой коллекции. |
| [get_FormatCode](./get_formatcode/)() | Получает или задает код формата, применяемый к значениям X. |
| [GetEnumerator](./getenumerator/)() override | Возвращает объект перечислителя. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Получает или задает значение X по указанному индексу. |
| [idx_set](./idx_set/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&) | Получает или задает значение X по указанному индексу. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FormatCode](./set_formatcode/)(const System::String\&) | Сеттер для [Aspose::Words::Drawing::Charts::ChartXValueCollection::get_FormatCode](./get_formatcode/). |
| static [Type](./type/)() |  |
## Примечания


Все элементы коллекции, кроме **null**, должны иметь одинаковый [ValueType](../chartxvalue/get_valuetype/).

Коллекция позволяет только изменять значения X. Чтобы добавить или вставить новые значения в ряд диаграммы, либо удалить значения, можно использовать соответствующие методы класса [ChartSeries](../chartseries/).

## Примеры



Показывает, как получить данные серии диаграммы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->idx_get(0);

double minValue = std::numeric_limits<double>::max();
int32_t minValueIndex = 0;
double maxValue = std::numeric_limits<double>::lowest();
int32_t maxValueIndex = 0;

for (int32_t i = 0; i < series->get_YValues()->get_Count(); i++)
{
    // Очистить индивидуальное форматирование всех точек данных.
    // Точки данных и их значения соответствуют один к одному в столбчатых диаграммах.
    series->get_DataPoints()->idx_get(i)->ClearFormat();

    // Получить значение Y.
    double yValue = series->get_YValues()->idx_get(i)->get_DoubleValue();

    if (yValue < minValue)
    {
        minValue = yValue;
        minValueIndex = i;
    }

    if (yValue > maxValue)
    {
        maxValue = yValue;
        maxValueIndex = i;
    }
}

// Изменить цвета максимального и минимального значений.
series->get_DataPoints()->idx_get(minValueIndex)->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Red());
series->get_DataPoints()->idx_get(maxValueIndex)->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Green());

doc->Save(get_ArtifactsDir() + u"Charts.GetChartSeriesData.docx");
```

## См. также

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
