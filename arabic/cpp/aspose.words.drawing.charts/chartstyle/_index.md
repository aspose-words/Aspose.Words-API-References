---
title: "Aspose::Words::Drawing::Charts::ChartStyle تعداد"
linktitle: "ChartStyle"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Charts::ChartStyle enum. يحدد الأنماط المحددة مسبقًا لمخطط في C++."
type: docs
weight: 27875
url: /ar/cpp/aspose.words.drawing.charts/chartstyle/
---
## ChartStyle enum


يحدد الأنماط المحددة مسبقًا للمخطط.

```cpp
enum class ChartStyle
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| عادي | 0 | يمثل نمط المخطط الافتراضي. |
| Muted | 1 | نمط بألوان خافتة. |
| Saturated | 2 | نمط بألوان أكثر تشبعًا. |
| Shaded | 3 | نمط بنقاط بيانات مظللة. |
| Flat | 4 | نمط بنقاط بيانات مسطحة بدون تدرج. |
| Shadowed | 5 | نمط بنقاط بيانات لها ظل. |
| تدرج | 6 | نمط بملء تدرجي لنقاط البيانات. |
| الأصلي | 7 | نمط بمظهر أصلي للمخطط. |
| Transparent1 | 8 | نمط بنقاط بيانات شفافة. |
| Transparent2 | 9 | نمط بنقاط بيانات شفافة. |
| Outline | 10 | نمط بنقاط بيانات لا تحتوي على تعبئة، بل فقط حدود. |
| OutlineBlack | 11 | نمط بخلفية مخطط سوداء، حيث لا تحتوي نقاط البيانات على تعبئة، بل فقط حدود. |
| أسود | 12 | نمط بخلفية مخطط سوداء. |
| Grey | 13 | نمط بخلفية مخطط بتدرج رمادي. |
| أزرق | 14 | نمط بخلفية مخطط زرقاء. |
| ShadedPlot | 15 | نمط، تكون فيه منطقة الرسم مظللة. |


## أمثلة



يعرض كيفية تعيين واسترجاع نمط المخطط.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إدراج مخطط بالنمط الأسود.
builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 400, 250, Aspose::Words::Drawing::Charts::ChartStyle::Black);

doc->Save(get_ArtifactsDir() + u"Charts.SetChartStyle.docx");

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Charts.SetChartStyle.docx");

// احصل على مخطط لتحديثه.
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// احصل على نمط المخطط.
ASSERT_EQ(Aspose::Words::Drawing::Charts::ChartStyle::Black, chart->get_Style());
```

## انظر أيضًا

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
