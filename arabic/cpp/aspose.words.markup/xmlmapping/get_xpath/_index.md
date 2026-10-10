---
title: "طريقة Aspose::Words::Markup::XmlMapping::get_XPath"
linktitle: "get_XPath"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Markup::XmlMapping::get_XPath. تُرجع تعبير XPath الذي يتم تقييمه للعثور على عقدة XML مخصصة يتم ربطها بالوسم الهيكلي للوثيقة الأصل في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.markup/xmlmapping/get_xpath/
---
## XmlMapping::get_XPath method


يعيد تعبير XPath الذي يُقيم للعثور على عقدة XML المخصصة التي تم ربطها بالعلامة المهيكلة للأب للمستند.

```cpp
System::String Aspose::Words::Markup::XmlMapping::get_XPath() const
```


## أمثلة



يعرض كيفية ضبط تعيينات XML لأجزاء XML المخصصة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// أنشئ جزء XML يحتوي على نص وأضفه إلى مجموعة CustomXmlPart في المستند.
System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Text element #1</text><text>Text element #2</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

ASSERT_EQ(u"<root><text>Text element #1</text><text>Text element #2</text></root>", System::Text::Encoding::get_UTF8()->GetString(xmlPart->get_Data()));

// أنشئ علامة مستند مهيكلة ستعرض محتويات CustomXmlPart الخاص بنا.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Block);

// اضبط ربطًا لعلامة المستند المهيكلة الخاصة بنا. هذا الربط سيُوجه
// علامة المستند المهيكلة الخاصة بنا لعرض جزء من محتويات نص جزء XML الذي يشير إليه XPath.
// في هذه الحالة، سيكون المحتوى هو العنصر \"<text>\" الثاني داخل العنصر \"<root>\" الأول: \"Text element #2\".
tag->get_XmlMapping()->SetMapping(xmlPart, u"/root[1]/text[2]", u"xmlns:ns='http://www.w3.org/2001/XMLSchema'");

ASSERT_TRUE(tag->get_XmlMapping()->get_IsMapped());
ASPOSE_ASSERT_EQ(xmlPart, tag->get_XmlMapping()->get_CustomXmlPart());
ASSERT_EQ(u"/root[1]/text[2]", tag->get_XmlMapping()->get_XPath());
ASSERT_EQ(u"xmlns:ns='http://www.w3.org/2001/XMLSchema'", tag->get_XmlMapping()->get_PrefixMappings());

// أضف علامة المستند المهيكلة إلى المستند لعرض المحتوى من الجزء المخصص الخاص بنا.
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);
doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.XmlMapping.docx");
```

## انظر أيضًا

* Class [XmlMapping](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
