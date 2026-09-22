---
title: "طريقة Aspose::Words::HeaderFooter::get_HeaderFooterType"
linktitle: "get_HeaderFooterType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::HeaderFooter::get_HeaderFooterType. يحصل على نوع هذه الترويسة/التذييل في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words/headerfooter/get_headerfootertype/
---
## HeaderFooter::get_HeaderFooterType method


يحصل على نوع هذا الرأس/التذييل.

```cpp
Aspose::Words::HeaderFooterType Aspose::Words::HeaderFooter::get_HeaderFooterType()
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

* Enum [HeaderFooterType](../../headerfootertype/)
* Class [HeaderFooter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
