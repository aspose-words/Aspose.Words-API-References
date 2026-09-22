---
title: "Aspose::Words::BorderCollection::idx_get method"
linktitle: "idx_get"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::BorderCollection::idx_get method. يسترجع كائن Border حسب نوع الحد في C++."
type: docs
weight: 18000
url: /ar/cpp/aspose.words/bordercollection/idx_get/
---
## BorderCollection::idx_get(Aspose::Words::BorderType) method


يسترجع كائن [Border](../../border/) حسب نوع الحد.

```cpp
System::SharedPtr<Aspose::Words::Border> Aspose::Words::BorderCollection::idx_get(Aspose::Words::BorderType borderType)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| borderType | Aspose::Words::BorderType | قيمة [BorderType](../../bordertype/) التي تحدد نوع الحد المراد استرجاعه. |
## ملاحظات


لاحظ أن ليس كل الحدود موجودة لعناصر المستند المختلفة. تُطلق هذه الطريقة استثناءً إذا طلبت حدًا غير قابل للتطبيق على الكائن الحالي.

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

## انظر أيضًا

* Class [Border](../../border/)
* Enum [BorderType](../../bordertype/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## BorderCollection::idx_get(int32_t) method


يسترجع كائن [Border](../../border/) حسب الفهرس.

```cpp
System::SharedPtr<Aspose::Words::Border> Aspose::Words::BorderCollection::idx_get(int32_t index)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| index | int32_t | الفهرس الصفري للحد المراد استرجاعه. |

## أمثلة



يظهر كيف يمكن لمجموعات الحدود مشاركة العناصر.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Paragraph 1.");
builder->Write(u"Paragraph 2.");

// نظرًا لأننا استخدمنا نفس إعدادات الحد أثناء الإنشاء
// هذه الفقرات، تشارك مجموعات حدودها نفس العناصر.
System::SharedPtr<Aspose::Words::BorderCollection> firstParagraphBorders = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Borders();
System::SharedPtr<Aspose::Words::BorderCollection> secondParagraphBorders = builder->get_CurrentParagraph()->get_ParagraphFormat()->get_Borders();

for (int32_t i = 0; i < firstParagraphBorders->get_Count(); i++)
{
    ASSERT_TRUE(System::ObjectExt::Equals(firstParagraphBorders->idx_get(i), secondParagraphBorders->idx_get(i)));
    ASSERT_EQ(System::ObjectExt::GetHashCode(firstParagraphBorders->idx_get(i)), System::ObjectExt::GetHashCode(secondParagraphBorders->idx_get(i)));
    ASSERT_FALSE(firstParagraphBorders->idx_get(i)->get_IsVisible());
}

for (auto&& border : System::IterateOver(secondParagraphBorders))
{
    border->set_LineStyle(Aspose::Words::LineStyle::DotDash);
}

// بعد تغيير نمط الخط للحدود في الفقرة الثانية فقط،
// لم تعد مجموعات الحدود تشارك نفس العناصر.
for (int32_t i = 0; i < firstParagraphBorders->get_Count(); i++)
{
    ASSERT_FALSE(System::ObjectExt::Equals(firstParagraphBorders->idx_get(i), secondParagraphBorders->idx_get(i)));
    ASSERT_NE(System::ObjectExt::GetHashCode(firstParagraphBorders->idx_get(i)), System::ObjectExt::GetHashCode(secondParagraphBorders->idx_get(i)));

    // تغيير مظهر حد فارغ يجعله مرئيًا.
    ASSERT_TRUE(secondParagraphBorders->idx_get(i)->get_IsVisible());
}

doc->Save(get_ArtifactsDir() + u"Border.SharedElements.docx");
```

## انظر أيضًا

* Class [Border](../../border/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
