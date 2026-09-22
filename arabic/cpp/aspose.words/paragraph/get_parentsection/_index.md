---
title: "Aspose::Words::Paragraph::get_ParentSection طريقة"
linktitle: "get_ParentSection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Paragraph::get_ParentSection طريقة. يسترجع القسم الأب للفقرة في C++."
type: docs
weight: 23000
url: /ar/cpp/aspose.words/paragraph/get_parentsection/
---
## Paragraph::get_ParentSection method


يسترجع القسم الأب [Section](../../section/) للفقرة.

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::Paragraph::get_ParentSection()
```


## أمثلة



يوضح كيفية إنشاء رأس وتذييل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// أنشئ رأسًا وأضف فقرةً إليه. النص في تلك الفقرة
// سيظهر في أعلى كل صفحة من هذا القسم، فوق النص الأساسي.
auto header = System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::HeaderPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(header);

System::SharedPtr<Aspose::Words::Paragraph> para = header->AppendParagraph(u"My header.");

ASSERT_TRUE(header->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

// أنشئ تذييلًا وأضف فقرةً إليه. النص في تلك الفقرة
// سيظهر في أسفل كل صفحة من هذا القسم، تحت النص الأساسي.
auto footer = System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::FooterPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(footer);

para = footer->AppendParagraph(u"My footer.");

ASSERT_FALSE(footer->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

ASPOSE_ASSERT_EQ(footer, para->get_ParentStory());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), para->get_ParentSection());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), header->get_ParentSection());

doc->Save(get_ArtifactsDir() + u"HeaderFooter.Create.docx");
```

## انظر أيضًا

* Class [Section](../../section/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
