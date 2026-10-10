---
title: "Aspose::Words::Drawing::Charts::ChartSeries::Remove طريقة"
linktitle: "Remove"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Charts::ChartSeries::Remove طريقة. يزيل قيمة X، قيمة Y، وحجم الفقاعات، إذا كان مدعومًا، من سلسلة المخطط عند الفهرس المحدد. كما يتم إزالة نقطة البيانات المقابلة وملصق البيانات أيضًا في C++."
type: docs
weight: 14500
url: /ar/cpp/aspose.words.drawing.charts/chartseries/remove/
---
## ChartSeries::Remove method


يزيل قيمة X وقيمة Y وحجم الفقاعة، إذا كان مدعومًا، من السلسلة البيانية عند الفهرس المحدد. كما يتم إزالة نقطة البيانات المقابلة وملصق البيانات.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeries::Remove(int32_t index)
```


## أمثلة



يعرض كيفية إضافة/إزالة قيم بيانات المخطط.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> department1Series = chart->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> department2Series = chart->get_Series()->idx_get(1);

// إزالة القيمة الأولى في كلا السلسلتين.
department1Series->Remove(0);
department2Series->Remove(0);

// إضافة قيم جديدة إلى كلا السلسلتين.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValue> newXCategory = Aspose::Words::Drawing::Charts::ChartXValue::FromString(u"Q1, 2023");
department1Series->Add(newXCategory, Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10.3));
department2Series->Add(newXCategory, Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(5.7));

doc->Save(get_ArtifactsDir() + u"Charts.ChartDataValues.docx");
```

## انظر أيضًا

* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
