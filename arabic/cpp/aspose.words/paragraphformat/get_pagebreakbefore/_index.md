---
title: "Aspose::Words::ParagraphFormat::get_PageBreakBefore طريقة"
linktitle: "get_PageBreakBefore"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::ParagraphFormat::get_PageBreakBefore طريقة. true إذا تم فرض فاصل صفحة قبل الفقرة في C++."
type: docs
weight: 27000
url: /ar/cpp/aspose.words/paragraphformat/get_pagebreakbefore/
---
## ParagraphFormat::get_PageBreakBefore method


صحيح إذا تم فرض فاصل صفحة قبل الفقرة.

```cpp
bool Aspose::Words::ParagraphFormat::get_PageBreakBefore()
```


## أمثلة



يوضح كيفية إنشاء فقرات مع فواصل صفحات في البداية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// اضبط هذه العلامة إلى "true" لتطبيق فاصل صفحة على بداية كل فقرة
// التي سيُنشئها مُنشئ المستند تحت تكوين ParagraphFormat هذا.
// الفقرة الأولى لن تتلقى فاصل صفحة.
// اترك هذه العلامة كـ "false" لبدء كل فقرة جديدة على نفس الصفحة
// كما السابق، بشرط وجود مساحة كافية.
builder->get_ParagraphFormat()->set_PageBreakBefore(pageBreakBefore);

builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");

auto layoutCollector = System::MakeObject<Aspose::Words::Layout::LayoutCollector>(doc);
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

if (pageBreakBefore)
{
    ASSERT_EQ(1, layoutCollector->GetStartPageIndex(paragraphs->idx_get(0)));
    ASSERT_EQ(2, layoutCollector->GetStartPageIndex(paragraphs->idx_get(1)));
}
else
{
    ASSERT_EQ(1, layoutCollector->GetStartPageIndex(paragraphs->idx_get(0)));
    ASSERT_EQ(1, layoutCollector->GetStartPageIndex(paragraphs->idx_get(1)));
}

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.PageBreakBefore.docx");
```

## انظر أيضًا

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
