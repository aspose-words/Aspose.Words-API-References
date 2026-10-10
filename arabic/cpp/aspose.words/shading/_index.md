---
title: "Aspose::Words::Shading فئة"
linktitle: "Shading"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Shading فئة. تحتوي على سمات التظليل لكائن. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 60000
url: /ar/cpp/aspose.words/shading/
---
## Shading class


يحتوي على سمات التظليل لكائن. لمعرفة المزيد، زر مقالة الوثائق [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class Shading : public Aspose::Words::InternableComplexAttr,
                public Aspose::Words::IComplexAttr
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | يزيل التظليل من الكائن. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Shading\>\&) | يحدد ما إذا كان [Shading](./) المحدد يساوي في القيمة [Shading](./) الحالي. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | يحدد ما إذا كان الكائن المحدد مساوٍ في القيمة للكائن الحالي. |
| [get_BackgroundPatternColor](./get_backgroundpatterncolor/)() | يحصل أو يعيّن اللون المطبق على خلفية كائن [Shading](./). |
| [get_BackgroundPatternThemeColor](./get_backgroundpatternthemecolor/)() | يحصل أو يعيّن لون نمط الخلفية في مخطط الألوان المطبق المرتبط بهذا كائن [Shading](./). |
| [get_BackgroundTintAndShade](./get_backgroundtintandshade/)() | يحصل أو يعيّن قيمة مزدوجة تُفتح أو تُغميق لون سمة الخلفية. |
| [get_ForegroundPatternColor](./get_foregroundpatterncolor/)() | الحصول أو تعيين اللون الذي يُطبق على المقدمة لكائن [Shading](./). |
| [get_ForegroundPatternThemeColor](./get_foregroundpatternthemecolor/)() | الحصول أو تعيين لون سمة نمط المقدمة في مخطط الألوان المطبق المرتبط بهذا الكائن [Shading](./). |
| [get_ForegroundTintAndShade](./get_foregroundtintandshade/)() | الحصول أو تعيين قيمة مزدوجة تُفتح أو تُغمق لون سمة المقدمة. |
| [get_Texture](./get_texture/)() | الحصول أو تعيين ملمس التظليل. |
| [GetHashCode](./gethashcode/)() const override | يعمل كدالة تجزئة لهذا النوع. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BackgroundPatternColor](./set_backgroundpatterncolor/)(System::Drawing::Color) | دالة تعيين لـ [Aspose::Words::Shading::get_BackgroundPatternColor](./get_backgroundpatterncolor/). |
| [set_BackgroundPatternThemeColor](./set_backgroundpatternthemecolor/)(Aspose::Words::Themes::ThemeColor) | دالة تعيين لـ [Aspose::Words::Shading::get_BackgroundPatternThemeColor](./get_backgroundpatternthemecolor/). |
| [set_BackgroundTintAndShade](./set_backgroundtintandshade/)(double) | دالة تعيين لـ [Aspose::Words::Shading::get_BackgroundTintAndShade](./get_backgroundtintandshade/). |
| [set_ForegroundPatternColor](./set_foregroundpatterncolor/)(System::Drawing::Color) | دالة تعيين لـ [Aspose::Words::Shading::get_ForegroundPatternColor](./get_foregroundpatterncolor/). |
| [set_ForegroundPatternThemeColor](./set_foregroundpatternthemecolor/)(Aspose::Words::Themes::ThemeColor) | دالة تعيين لـ [Aspose::Words::Shading::get_ForegroundPatternThemeColor](./get_foregroundpatternthemecolor/). |
| [set_ForegroundTintAndShade](./set_foregroundtintandshade/)(double) | دالة تعيين لـ [Aspose::Words::Shading::get_ForegroundTintAndShade](./get_foregroundtintandshade/). |
| [set_Texture](./set_texture/)(Aspose::Words::TextureIndex) | دالة تعيين لـ [Aspose::Words::Shading::get_Texture](./get_texture/). |
| static [Type](./type/)() |  |

## أمثلة



يوضح كيفية تطبيق لون الحدود والتظليل أثناء بناء جدول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// ابدأ جدولًا وحدد لونًا/سماكةً افتراضيةً لحدوده.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
table->SetBorders(Aspose::Words::LineStyle::Single, 2.0, System::Drawing::Color::get_Black());

// أنشئ صفًا يحتوي على خليتين بألوان خلفية مختلفة.
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightSkyBlue());
builder->Writeln(u"Row 1, Cell 1.");
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_Orange());
builder->Writeln(u"Row 1, Cell 2.");
builder->EndRow();

// إعادة تعيين تنسيق الخلية لتعطيل ألوان الخلفية
// حدد سماكة حد مخصصة لجميع الخلايا الجديدة التي ينشئها المُنشئ،
// ثم أنشئ صفًا ثانيًا.
builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->get_Borders()->get_Left()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Right()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Top()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Bottom()->set_LineWidth(4.0);

builder->InsertCell();
builder->Writeln(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Writeln(u"Row 2, Cell 2.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.TableBordersAndShading.docx");
```


يوضح كيفية تزيين النص بالحدود والتظليل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::BorderCollection> borders = builder->get_ParagraphFormat()->get_Borders();
borders->set_DistanceFromText(20);
borders->idx_get(Aspose::Words::BorderType::Left)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Right)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Top)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Bottom)->set_LineStyle(Aspose::Words::LineStyle::Double);

System::SharedPtr<Aspose::Words::Shading> shading = builder->get_ParagraphFormat()->get_Shading();
shading->set_Texture(Aspose::Words::TextureIndex::TextureDiagonalCross);
shading->set_BackgroundPatternColor(System::Drawing::Color::get_LightCoral());
shading->set_ForegroundPatternColor(System::Drawing::Color::get_LightSalmon());

builder->Write(u"This paragraph is formatted with a double border and shading.");
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.ApplyBordersAndShading.docx");
```

## انظر أيضًا

* Class [InternableComplexAttr](../internablecomplexattr/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
