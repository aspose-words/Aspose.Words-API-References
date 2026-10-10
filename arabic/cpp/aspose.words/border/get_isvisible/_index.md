---
title: "طريقة Aspose::Words::Border::get_IsVisible"
linktitle: "get_IsVisible"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Border::get_IsVisible. تُرجع **true** إذا كان LineStyle ليس None في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words/border/get_isvisible/
---
## Border::get_IsVisible method


تُرجع **true** إذا كان [LineStyle](../get_linestyle/) ليس [None](../../linestyle/).

```cpp
bool Aspose::Words::Border::get_IsVisible()
```


## أمثلة



يظهر كيفية إزالة الحدود من فقرة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Borders.docx");

// كل فقرة لديها مجموعة فردية من الحدود.
// يمكننا الوصول إلى إعدادات مظهر هذه الحدود عبر كائن تنسيق الفقرة.
System::SharedPtr<Aspose::Words::BorderCollection> borders = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Borders();

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), borders->idx_get(0)->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(3.0, borders->idx_get(0)->get_LineWidth());
ASSERT_EQ(Aspose::Words::LineStyle::Single, borders->idx_get(0)->get_LineStyle());
ASSERT_TRUE(borders->idx_get(0)->get_IsVisible());

// يمكننا إزالة حد مرة واحدة عن طريق تشغيل طريقة ClearFormatting.
// تشغيل هذه الطريقة على كل حد في الفقرة سيزيل جميع حدوده.
for (auto&& border : System::IterateOver(borders))
{
    border->ClearFormatting();
}

ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), borders->idx_get(0)->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(0.0, borders->idx_get(0)->get_LineWidth());
ASSERT_EQ(Aspose::Words::LineStyle::None, borders->idx_get(0)->get_LineStyle());
ASSERT_FALSE(borders->idx_get(0)->get_IsVisible());

doc->Save(get_ArtifactsDir() + u"Border.ClearFormatting.docx");
```

## انظر أيضًا

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
