---
title: "Aspose::Words::Border::Equals طريقة"
linktitle: "Equals"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Border::Equals طريقة. يحدد ما إذا كان الحد المحدد يساوي في القيمة الحد الحالي في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words/border/equals/
---
## Border::Equals(const System::SharedPtr\<Aspose::Words::Border\>\&) method


يحدد ما إذا كان الحد المحدد مساويًا في القيمة للحد الحالي.

```cpp
bool Aspose::Words::Border::Equals(const System::SharedPtr<Aspose::Words::Border> &rhs)
```


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

* Class [Border](../)
* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Border::Equals(System::SharedPtr\<System::Object\>) method


يحدد ما إذا كان الكائن المحدد مساوٍ في القيمة للكائن الحالي.

```cpp
bool Aspose::Words::Border::Equals(System::SharedPtr<System::Object> obj) override
```


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

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
