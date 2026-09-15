---
title: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_XmlMapping طريقة"
linktitle: "get_XmlMapping"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_XmlMapping طريقة. يحصل على كائن يمثل تعيين هذا النطاق لعلامة المستند المهيكلة إلى بيانات XML في جزء XML مخصص للمستند الحالي في C++."
type: docs
weight: 21000
url: /ar/cpp/aspose.words.markup/structureddocumenttagrangestart/get_xmlmapping/
---
## StructuredDocumentTagRangeStart::get_XmlMapping method


يحصل على كائن يمثل ربط نطاق وسم المستند المنسق ببيانات XML في جزء XML مخصص للمستند الحالي.

```cpp
System::SharedPtr<Aspose::Words::Markup::XmlMapping> Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_XmlMapping() override
```


## أمثلة



يعرض كيفية تعيين تعيينات XML لبداية النطاق لعلامة مستند مهيكلة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");

// أنشئ جزء XML يحتوي على نص وأضفه إلى مجموعة CustomXmlPart في المستند.
System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Text element #1</text><text>Text element #2</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

ASSERT_EQ(u"<root><text>Text element #1</text><text>Text element #2</text></root>", System::Text::Encoding::get_UTF8()->GetString(xmlPart->get_Data()));

// إنشاء علامة مستند منسقة ستعرض محتويات CustomXmlPart الخاص بنا في المستند.
auto sdtRangeStart = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, 0, true));

// إذا قمنا بتعيين تخطيط لعلامة المستند المنسقة الخاصة بنا،
// فإنها ستعرض فقط جزءًا من CustomXmlPart الذي يشير إليه XPath.
// سوف يشير هذا XPath إلى العنصر الثاني "<text>" من محتويات العنصر الأول "<root>" في CustomXmlPart الخاص بنا.
sdtRangeStart->get_XmlMapping()->SetMapping(xmlPart, u"/root[1]/text[2]", nullptr);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.StructuredDocumentTagRangeStartXmlMapping.docx");
```

## انظر أيضًا

* Class [XmlMapping](../../xmlmapping/)
* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
