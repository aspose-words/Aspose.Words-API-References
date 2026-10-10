---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Font طريقة"
linktitle: "get_Font"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Font طريقة. يوفر الوصول إلى تنسيق الخط لتسميات البيانات للسلسلة بأكملها في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_font/
---
## ChartDataLabelCollection::get_Font method


يوفر الوصول إلى تنسيق الخط لتسميات البيانات للسلسلة بأكملها.

```cpp
System::SharedPtr<Aspose::Words::Font> Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Font()
```


## أمثلة



يعرض كيفية تمكين وتكوين تسميات البيانات لسلسلة مخطط.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أضف مخطط خطي، ثم امسح سلسلة البيانات التجريبية الخاصة به للبدء بمخطط نظيف،
// ثم قم بتعيين عنوان.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
chart->get_Series()->Clear();
chart->get_Title()->set_Text(u"Monthly sales report");

// أدرج سلسلة مخطط مخصصة مع الأشهر كفئات للمحور X،
// ومبالغ عشرية مقابلة للمحور Y.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Revenue", System::MakeArray<System::String>({u"January", u"February", u"March"}), System::MakeArray<double>({25.611, 21.439, 33.750}));

// فعّل تسميات البيانات، ثم طبّق تنسيق رقم مخصص للقيم المعروضة في تسميات البيانات.
// سيعامل هذا التنسيق القيم العشرية المعروضة كملّيين من الدولار الأمريكي.
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowValue(true);
dataLabels->get_NumberFormat()->set_FormatCode(u"\"US$\" #,##0.000\"M\"");
dataLabels->get_Font()->set_Size(12);

doc->Save(get_ArtifactsDir() + u"Charts.DataLabelNumberFormat.docx");
```

## انظر أيضًا

* Class [Font](../../../aspose.words/font/)
* Class [ChartDataLabelCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
