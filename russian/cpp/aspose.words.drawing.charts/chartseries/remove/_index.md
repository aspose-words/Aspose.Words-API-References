---
title: "Aspose::Words::Drawing::Charts::ChartSeries::Remove метод"
linktitle: "Remove"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::ChartSeries::Remove метод. Удаляет значение X, значение Y и размер пузыря, если поддерживается, из серии диаграммы по указанному индексу. Соответствующая точка данных и подпись к данным также удаляются в C++."
type: docs
weight: 14500
url: /ru/cpp/aspose.words.drawing.charts/chartseries/remove/
---
## ChartSeries::Remove method


Удаляет значение X, значение Y и размер пузыря (если поддерживается) из серии диаграммы в указанном индексе. Соответствующая точка данных и подпись данных также удаляются.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeries::Remove(int32_t index)
```


## Примеры



Показывает, как добавить/удалить значения данных диаграммы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> department1Series = chart->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> department2Series = chart->get_Series()->idx_get(1);

// Удалите первое значение в обеих сериях.
department1Series->Remove(0);
department2Series->Remove(0);

// Добавьте новые значения в обе серии.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValue> newXCategory = Aspose::Words::Drawing::Charts::ChartXValue::FromString(u"Q1, 2023");
department1Series->Add(newXCategory, Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10.3));
department2Series->Add(newXCategory, Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(5.7));

doc->Save(get_ArtifactsDir() + u"Charts.ChartDataValues.docx");
```

## См. также

* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
