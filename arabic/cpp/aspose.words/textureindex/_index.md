---
title: "Aspose::Words::TextureIndex enum"
linktitle: "TextureIndex"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::TextureIndex enum. يحدد نسيج التظليل في C++."
type: docs
weight: 125000
url: /ar/cpp/aspose.words/textureindex/
---
## TextureIndex enum


يحدد نسيج التظليل.

```cpp
enum class TextureIndex
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| Texture10Percent | 3 |  |
| Texture12Pt5Percent | 37 |  |
| Texture15Percent | 38 |  |
| Texture17Pt5Percent | 39 |  |
| Texture20Percent | 4 |  |
| Texture22Pt5Percent | 40 |  |
| Texture25Percent | 5 |  |
| Texture27Pt5Percent | 41 |  |
| Texture2Pt5Percent | 35 |  |
| Texture30Percent | 6 |  |
| Texture32Pt5Percent | 42 |  |
| Texture35Percent | 43 |  |
| الملمس37Pt5٪ | 44 |  |
| الملمس40٪ | 7 |  |
| الملمس42Pt5٪ | 45 |  |
| الملمس45٪ | 46 |  |
| الملمس47Pt5٪ | 47 |  |
| الملمس50٪ | 8 |  |
| الملمس52Pt5٪ | 48 |  |
| الملمس55٪ | 49 |  |
| الملمس57Pt5٪ | 50 |  |
| الملمس5٪ | 2 |  |
| الملمس60٪ | 9 |  |
| الملمس62Pt5٪ | 51 |  |
| الملمس65٪ | 52 |  |
| الملمس67Pt5٪ | 53 |  |
| الملمس70٪ | 10 |  |
| الملمس72Pt5٪ | 54 |  |
| الملمس75٪ | 11 |  |
| الملمس77Pt5٪ | 55 |  |
| الملمس7Pt5٪ | 36 |  |
| الملمس80٪ | 12 |  |
| الملمس82Pt5٪ | 56 |  |
| الملمس85٪ | 57 |  |
| الملمس87Pt5٪ | 58 |  |
| الملمس90٪ | 13 |  |
| الملمس92Pt5٪ | 59 |  |
| Texture95Percent | 60 |  |
| Texture97Pt5Percent | 61 |  |
| TextureCross | 24 |  |
| TextureDarkCross | 18 |  |
| TextureDarkDiagonalCross | 19 |  |
| TextureDarkDiagonalDown | 16 |  |
| TextureDarkDiagonalUp | 17 |  |
| TextureDarkHorizontal | 14 |  |
| TextureDarkVertical | 15 |  |
| TextureDiagonalCross | 25 |  |
| TextureDiagonalDown | 22 |  |
| TextureDiagonalUp | 23 |  |
| TextureHorizontal | 20 |  |
| TextureNone | 0 |  |
| TextureSolid | 1 |  |
| TextureVertical | 21 |  |
| TextureNil | 65535 | يحدد أنه لا ينبغي استخدام أي نمط في المنطقة المظللة الحالية (أي أن النمط يجب أن يكون تعبئة كاملة بلون الخلفية). |


## أمثلة



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


يظهر كيفية تطبيق حد خارجي على جدول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// محاذاة الجدول إلى مركز الصفحة.
table->set_Alignment(Aspose::Words::Tables::TableAlignment::Center);

// مسح أي حدود أو تظليل موجودة من الجدول.
table->ClearBorders();
table->ClearShading();

// إضافة حدود خضراء إلى الإطار الخارجي للجدول.
table->SetBorder(Aspose::Words::BorderType::Left, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Right, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Top, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Bottom, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);

// ملء الخلايا بلون أخضر فاتح صلب.
table->SetShading(Aspose::Words::TextureIndex::TextureSolid, System::Drawing::Color::get_LightGreen(), System::Drawing::Color::Empty);

doc->Save(get_ArtifactsDir() + u"Table.SetOutlineBorders.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
