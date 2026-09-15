---
title: "Aspose::Words::Markup::XmlMapping class"
linktitle: "XmlMapping"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Markup::XmlMapping class. يحدد المعلومات التي تُستخدم لإنشاء ربط بين العلامة المهيكلة للأب للمستند وعنصر XML مخزن داخل جزء بيانات XML مخصص في المستند. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 15000
url: /ar/cpp/aspose.words.markup/xmlmapping/
---
## XmlMapping class


يحدد المعلومات المستخدمة لإنشاء ربط بين علامة المستند المُنظمة الأصلية وعنصر XML المخزن داخل جزء بيانات XML مخصص في المستند. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class XmlMapping : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Delete](./delete/)() | يحذف ربط المستند المهيكل الأب ببيانات XML. |
| [get_CustomXmlPart](./get_customxmlpart/)() | يعيد جزء بيانات XML المخصص الذي تم ربطه بالعلامة المهيكلة للأب للمستند. |
| [get_IsMapped](./get_ismapped/)() | يعيد **true** إذا تم ربط العلامة المهيكلة للأب للمستند ببيانات XML بنجاح. |
| [get_PrefixMappings](./get_prefixmappings/)() const | يعيد تعيينات بادئات مساحة الاسم XML لتقييم [XPath](./get_xpath/). |
| [get_StoreItemId](./get_storeitemid/)() | يحدد معرف بيانات XML المخصص لجزء بيانات XML المخصص الذي سيُستخدم لتقييم تعبير [XPath](./get_xpath/). |
| [get_XPath](./get_xpath/)() const | يعيد تعبير XPath الذي يُقيم للعثور على عقدة XML المخصصة التي تم ربطها بالعلامة المهيكلة للأب للمستند. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [SetMapping](./setmapping/)(const System::SharedPtr\<Aspose::Words::Markup::CustomXmlPart\>\&, const System::String\&, const System::String\&) | يضبط ربطًا بين العلامة المهيكلة للأب للمستند وعقدة XML لجزء بيانات XML مخصص. |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
