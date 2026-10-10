---
title: "منشئ Aspose::Words::HeaderFooter::HeaderFooter"
linktitle: "HeaderFooter"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "منشئ Aspose::Words::HeaderFooter::HeaderFooter. ينشئ ترويسة أو تذييل جديد من النوع المحدد في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words/headerfooter/headerfooter/
---
## HeaderFooter::HeaderFooter constructor


ينشئ رأسًا أو تذييلًا جديدًا من النوع المحدد.

```cpp
Aspose::Words::HeaderFooter::HeaderFooter(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, Aspose::Words::HeaderFooterType headerFooterType)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | المستند المالك. |
| headerFooterType | Aspose::Words::HeaderFooterType | قيمة [HeaderFooterType](../get_headerfootertype/) التي تحدد نوع الترويسة أو التذييل. |
## ملاحظات


عند إنشاء [HeaderFooter](../)، ينتمي إلى المستند المحدد، لكنه ليس جزءًا من المستند بعد و[ParentNode](../../node/get_parentnode/) هو **null**.

لإضافة [HeaderFooter](../) إلى [Section](../../section/) استخدم [InsertAfter1()</see>, <see cref="Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertBefore1()](../)، أو خاصية [HeadersFooters](../../section/get_headersfooters/) والطرق [Add()](../)، [Insert()](../).

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

* Class [DocumentBase](../../documentbase/)
* Enum [HeaderFooterType](../../headerfootertype/)
* Class [HeaderFooter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
