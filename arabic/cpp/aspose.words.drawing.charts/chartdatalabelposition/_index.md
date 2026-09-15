---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelPosition enum"
linktitle: "ChartDataLabelPosition"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelPosition enum. يحدد الموضع لتسمية بيانات المخطط في C++."
type: docs
weight: 27334
url: /ar/cpp/aspose.words.drawing.charts/chartdatalabelposition/
---
## ChartDataLabelPosition enum


يحدد الموقع لتسمية بيانات المخطط.

```cpp
enum class ChartDataLabelPosition
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| وسط | 0 | يحدد أن تسمية البيانات يجب أن تُعرض في مركز علامة البيانات. |
| يسار | 1 | يحدد أن تسمية البيانات يجب أن تُعرض إلى يسار علامة البيانات. |
| يمين | 2 | يحدد أن تسمية البيانات يجب أن تُعرض إلى يمين علامة البيانات. |
| أعلى | 3 | يحدد أن تسمية البيانات يجب أن تُعرض فوق علامة البيانات. |
| أسفل | 4 | يحدد أن تسمية البيانات يجب أن تُعرض أسفل علامة البيانات. |
| InsideBase | 5 | يحدد أن تسمية البيانات يجب أن تُعرض داخل قاعدة علامة البيانات. |
| InsideEnd | 6 | يحدد أن تسمية البيانات يجب أن تُعرض داخل نهاية علامة البيانات. |
| OutsideEnd | 7 | يحدد أنه يجب عرض تسمية البيانات خارج نهاية علامة البيانات. |
| BestFit | 8 | يحدد أنه يجب عرض تسمية البيانات في الموقع الأنسب. |


## أمثلة



يظهر كيفية ضبط موضع تسمية البيانات.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إدراج مخطط عمودي.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();

// حذف السلسلة التي تم إنشاؤها افتراضيًا.
seriesColl->Clear();

// إضافة سلسلة.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = seriesColl->Add(u"Series 1", System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3"}), System::MakeArray<double>({4, 5, 6}));

// إظهار تسميات البيانات وتعيين لون الخط.
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowValue(true);
dataLabels->get_Font()->set_Color(System::Drawing::Color::get_White());

// ضبط موضع تسمية البيانات.
dataLabels->set_Position(Aspose::Words::Drawing::Charts::ChartDataLabelPosition::InsideBase);
dataLabels->idx_get(0)->set_Position(Aspose::Words::Drawing::Charts::ChartDataLabelPosition::OutsideEnd);
dataLabels->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_DarkRed());

doc->Save(get_ArtifactsDir() + u"Charts.LabelPosition.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
