---
title: "Aspose::Words::Drawing::Charts::ChartSeriesCollection class"
linktitle: "ChartSeriesCollection"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::ChartSeriesCollection class. Представляет коллекцию объектов ChartSeries. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 17000
url: /ru/cpp/aspose.words.drawing.charts/chartseriescollection/
---
## ChartSeriesCollection class


Представляет коллекцию [ChartSeries](../chartseries/). Чтобы узнать больше, посетите статью документации [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartSeriesCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries>>
```

## Методы

| Метод | Описание |
| --- | --- |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<double\>\&) | Добавляет новый [ChartSeries](../chartseries/) в эту коллекцию. Используйте этот метод, чтобы добавить серии к любому типу Bar, Column, Line и Surface диаграмм. |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<bool\>\&) |  |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<double\>\&) | Добавляет новый [ChartSeries](../chartseries/) в эту коллекцию. Используйте этот метод, чтобы добавить серии к любому типу диаграмм Scatter. |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<System::DateTime\>\&, const System::ArrayPtr\<double\>\&) | Добавляет новый [ChartSeries](../chartseries/) в эту коллекцию. Используйте этот метод, чтобы добавить серии к любому типу Area, Radar и Stock диаграмм. |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<double\>\&) | Добавляет новый [ChartSeries](../chartseries/) в эту коллекцию. Используйте этот метод, чтобы добавить серии к любому типу Bubble диаграмм. |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartMultilevelValue\>\>\&, const System::ArrayPtr\<double\>\&) | Добавляет новый [ChartSeries](../chartseries/) в эту коллекцию. Используйте этот метод, чтобы добавить серии с многоуровневыми категориями данных. |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<double\>\&) | Добавляет новый [ChartSeries](../chartseries/) в эту коллекцию. Используйте этот метод, чтобы добавить серии к Histogram диаграмм. |
| [Clear](./clear/)() | Удаляет все [ChartSeries](../chartseries/) из этой коллекции. |
| [get_Count](./get_count/)() | Возвращает количество [ChartSeries](../chartseries/) в этой коллекции. |
| [GetEnumerator](./getenumerator/)() override | Возвращает объект перечислителя. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Возвращает [ChartSeries](../chartseries/) по указанному индексу. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveAt](./removeat/)(int32_t) | Удаляет [ChartSeries](../chartseries/) по указанному индексу. |
| static [Type](./type/)() |  |

## Примеры



Показывает, как добавлять и удалять данные серии в диаграмме.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте столбчатую диаграмму, которая по умолчанию будет содержать три серии демонстрационных данных.
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Каждая серия содержит четыре десятичных значения: по одному для каждой из четырёх категорий.
// Четыре кластера по три столбца отобразят эти данные.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> chartData = chart->get_Series();

ASSERT_EQ(3, chartData->get_Count());

// Выведите название каждой серии на диаграмме.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries>>> enumerator = chart->get_Series()->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << enumerator->get_Current()->get_Name() << std::endl;
    }
}

// Это названия категорий на диаграмме.
System::ArrayPtr<System::String> categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3", u"Category 4"});

// Мы можем добавить серию с новыми значениями для существующих категорий.
// Эта диаграмма теперь будет содержать четыре кластера по четыре столбца.
chart->get_Series()->Add(u"Series 4", categories, System::MakeArray<double>({4.4, 7.0, 3.5, 2.1}));

// Серию диаграммы также можно удалить по индексу, как показано.
// Это удалит одну из трёх демонстрационных серий, поставляемых с диаграммой.
chartData->RemoveAt(2);

ASSERT_FALSE(chartData->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> s) -> bool
{
    return s->get_Name() == u"Series 3";
}))));

// Мы также можем очистить все данные диаграммы сразу с помощью этого метода.
// При создании новой диаграммы это способ удалить все демонстрационные данные
// перед тем как мы сможем начать работу с пустой диаграммой.
chartData->Clear();
```

## См. также

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
