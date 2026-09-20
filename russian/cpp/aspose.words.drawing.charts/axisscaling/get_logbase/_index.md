---
title: "Метод Aspose::Words::Drawing::Charts::AxisScaling::get_LogBase"
linktitle: "get_LogBase"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::Charts::AxisScaling::get_LogBase. Получает или задает логарифмическую основу для логарифмической оси в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.drawing.charts/axisscaling/get_logbase/
---
## AxisScaling::get_LogBase method


Получает или задает логарифмическую основу для логарифмической оси.

```cpp
double Aspose::Words::Drawing::Charts::AxisScaling::get_LogBase() const
```

## Примечания


Это свойство не поддерживается новыми диаграммами MS Office 2016.

Допустимый диапазон значения с плавающей точкой — больше или равно 2 и меньше или равно 1000. Свойство действует только если [Type](../get_type/) установлен в [Logarithmic](../../axisscaletype/).

Установка этого свойства задаёт свойство [Type](../get_type/) как [Logarithmic](../../axisscaletype/).

## Примеры



Показывает, как применить логарифмическое масштабирование к оси диаграммы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 450, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Очистите демонстрационную серию данных диаграммы, чтобы начать с чистой диаграммы.
chart->get_Series()->Clear();

// Вставьте серию с координатами X/Y для пяти точек.
chart->get_Series()->Add(u"Series 1", System::MakeArray<double>({1.0, 2.0, 3.0, 4.0, 5.0}), System::MakeArray<double>({1.0, 20.0, 400.0, 8000.0, 160000.0}));

// Масштабирование оси X по умолчанию линейное,
// отображая равномерно увеличивающиеся значения, охватывающие наш диапазон X (0, 1, 2, 3...).
// Линейная ось не идеальна для наших значений Y
// поскольку точки с меньшими значениями Y будет труднее читать.
// Логарифмическое масштабирование с основанием 20 (1, 20, 400, 8000...)
// распространит построенные точки, позволяя легче считывать их значения на диаграмме.
chart->get_AxisY()->get_Scaling()->set_Type(Aspose::Words::Drawing::Charts::AxisScaleType::Logarithmic);
chart->get_AxisY()->get_Scaling()->set_LogBase(20);

doc->Save(get_ArtifactsDir() + u"Charts.AxisScaling.docx");
```

## См. также

* Class [AxisScaling](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
