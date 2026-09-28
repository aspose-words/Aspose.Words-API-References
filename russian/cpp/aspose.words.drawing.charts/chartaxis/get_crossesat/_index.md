---
title: "Aspose::Words::Drawing::Charts::ChartAxis::get_CrossesAt метод"
linktitle: "get_CrossesAt"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::ChartAxis::get_CrossesAt method. Указывает, где на перпендикулярной оси ось пересекается в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.drawing.charts/chartaxis/get_crossesat/
---
## ChartAxis::get_CrossesAt method


Указывает, где на перпендикулярной оси происходит пересечение оси.

```cpp
double Aspose::Words::Drawing::Charts::ChartAxis::get_CrossesAt()
```

## Примечания


Свойство действует только если [Crosses](../get_crosses/) установлены в значение [Custom](../../axiscrosses/). Оно не поддерживается новыми диаграммами MS Office 2016.

Единицы измерения определяются типом оси. Когда ось является осью значений, значение свойства представляет собой десятичное число на оси значений. Когда ось является осью временных категорий, значение задаётся как целое число дней относительно базовой даты (30/12/1899). Для оси текстовых категорий значение представляет собой целый номер категории, начиная с 1 как первой категории.

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
