---
title: "Aspose::Words::Drawing::PresetTexture enum"
linktitle: "PresetTexture"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::PresetTexture enum. يحدد النسيج المستخدم لملء شكل في C++."
type: docs
weight: 32000
url: /ar/cpp/aspose.words.drawing/presettexture/
---
## PresetTexture enum


يحدد النسيج الذي سيُستخدم لملء الشكل.

```cpp
enum class PresetTexture
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| None | -1 | بدون نسيج. |
| BlueTissuePaper | 1 | نسيج ورق مناديل أزرق. |
| Bouquet | 2 | نسيج باقة. |
| BrownMarble | 3 | قوام رخام بني. |
| Canvas | 4 | قوام القماش. |
| Cork | 5 | قوام الفلين. |
| Denim | 6 | قوام الجينز. |
| FishFossil | 7 | قوام أحفار الأسماك. |
| Granite | 8 | قوام الجرانيت. |
| GreenMarble | 9 | قوام رخام أخضر. |
| MediumWood | 10 | قوام الخشب المتوسط. |
| Newsprint | 11 | قوام ورق الصحف. |
| Oak | 12 | قوام البلوط. |
| PaperBag | 13 | قوام كيس الورق. |
| Papyrus | 14 | قوام البردي. |
| Parchment | 15 | قوام الرق. |
| PinkTissuePaper | 16 | قوام ورق نسيج وردي. |
| PurpleMesh | 17 | قوام شبكة أرجوانية. |
| RecycledPaper | 18 | قوام ورق معاد تدويره. |
| رمل | 19 | قوام رمل. |
| قرطاسية | 20 | قوام قرطاسية. |
| جوز | 21 | قوام جوز. |
| WaterDroplets | 22 | قوام قطرات ماء. |
| WhiteMarble | 23 | قوام رخام أبيض. |
| WovenMat | 24 | قوام حصيرة منسوجة. |


## أمثلة



إظهار كيفية تعيين تنسيق العلامة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// حذف السلسلة التي تم إنشاؤها افتراضيًا.
chart->get_Series()->Clear();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"AW Series 1", System::MakeArray<double>({0.7, 1.8, 2.6, 3.9}), System::MakeArray<double>({2.7, 3.2, 0.8, 1.7}));

// تعيين تنسيق العلامة.
series->get_Marker()->set_Size(40);
series->get_Marker()->set_Symbol(Aspose::Words::Drawing::Charts::MarkerSymbol::Square);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataPointCollection> dataPoints = series->get_DataPoints();
dataPoints->idx_get(0)->get_Marker()->get_Format()->get_Fill()->PresetTextured(Aspose::Words::Drawing::PresetTexture::Denim);
dataPoints->idx_get(0)->get_Marker()->get_Format()->get_Stroke()->set_ForeColor(System::Drawing::Color::get_Yellow());
dataPoints->idx_get(0)->get_Marker()->get_Format()->get_Stroke()->set_BackColor(System::Drawing::Color::get_Red());
dataPoints->idx_get(1)->get_Marker()->get_Format()->get_Fill()->PresetTextured(Aspose::Words::Drawing::PresetTexture::WaterDroplets);
dataPoints->idx_get(1)->get_Marker()->get_Format()->get_Stroke()->set_ForeColor(System::Drawing::Color::get_Yellow());
dataPoints->idx_get(1)->get_Marker()->get_Format()->get_Stroke()->set_Visible(false);
dataPoints->idx_get(2)->get_Marker()->get_Format()->get_Fill()->PresetTextured(Aspose::Words::Drawing::PresetTexture::GreenMarble);
dataPoints->idx_get(2)->get_Marker()->get_Format()->get_Stroke()->set_ForeColor(System::Drawing::Color::get_Yellow());
dataPoints->idx_get(3)->get_Marker()->get_Format()->get_Fill()->PresetTextured(Aspose::Words::Drawing::PresetTexture::Oak);
dataPoints->idx_get(3)->get_Marker()->get_Format()->get_Stroke()->set_ForeColor(System::Drawing::Color::get_Yellow());
dataPoints->idx_get(3)->get_Marker()->get_Format()->get_Stroke()->set_Transparency(0.5);

doc->Save(get_ArtifactsDir() + u"Charts.MarkerFormatting.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
