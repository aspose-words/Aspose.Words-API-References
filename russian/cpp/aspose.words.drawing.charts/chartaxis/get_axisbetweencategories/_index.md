---
title: "Aspose::Words::Drawing::Charts::ChartAxis::get_AxisBetweenCategories метод"
linktitle: "get_AxisBetweenCategories"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::ChartAxis::get_AxisBetweenCategories метод. Получает или задает флаг, указывающий, пересекает ли ось значений ось категорий между категориями в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.drawing.charts/chartaxis/get_axisbetweencategories/
---
## ChartAxis::get_AxisBetweenCategories method


Получает или задает флаг, указывающий, пересекает ли ось значений ось категорий между категориями.

```cpp
bool Aspose::Words::Drawing::Charts::ChartAxis::get_AxisBetweenCategories()
```


## Примеры



Показывает, как заставить ось графика пересекаться в пользовательском месте.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(3, chart->get_Series()->get_Count());
ASSERT_EQ(u"Series 1", chart->get_Series()->idx_get(0)->get_Name());
ASSERT_EQ(u"Series 2", chart->get_Series()->idx_get(1)->get_Name());
ASSERT_EQ(u"Series 3", chart->get_Series()->idx_get(2)->get_Name());

// Для столбчатых диаграмм ось Y по умолчанию пересекает ноль,
// что означает, что столбцы для всех значений ниже нуля опускаются вниз, чтобы представить отрицательные значения.
// Мы можем задать другое значение пересечения оси Y. В данном случае мы установим его равным 3.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> axis = chart->get_AxisX();
axis->set_Crosses(Aspose::Words::Drawing::Charts::AxisCrosses::Custom);
axis->set_CrossesAt(3);
axis->set_AxisBetweenCategories(true);

doc->Save(get_ArtifactsDir() + u"Charts.AxisCross.docx");
```

## См. также

* Class [ChartAxis](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
