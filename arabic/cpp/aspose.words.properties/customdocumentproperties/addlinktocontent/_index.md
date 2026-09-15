---
title: "Aspose::Words::Properties::CustomDocumentProperties::AddLinkToContent method"
linktitle: "AddLinkToContent"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Properties::CustomDocumentProperties::AddLinkToContent method. ينشئ خاصية مستند مخصصة مرتبطة بالمحتوى جديدة في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.properties/customdocumentproperties/addlinktocontent/
---
## CustomDocumentProperties::AddLinkToContent method


ينشئ خاصية مستند مخصصة مرتبطة بالمحتوى جديدة.

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::CustomDocumentProperties::AddLinkToContent(const System::String &name, const System::String &linkSource)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| name | const System::String\& | اسم الخاصية. |
| linkSource | const System::String\& | مصدر الخاصية. |

### ReturnValue

كائن الخاصية الذي تم إنشاؤه حديثًا أو **null** عندما يكون *linkSource* غير صالح.

## أمثلة



يوضح كيفية ربط خاصية مستند مخصصة بإشارة مرجعية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartBookmark(u"MyBookmark");
builder->Write(u"Hello world!");
builder->EndBookmark(u"MyBookmark");

// ربط خاصية مخصصة جديدة بإشارة مرجعية. قيمة هذه الخاصية
// ستكون محتويات الإشارة المرجعية التي يشير إليها في العنصر "LinkSource".
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> customProperties = doc->get_CustomDocumentProperties();
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> customProperty = customProperties->AddLinkToContent(u"Bookmark", u"MyBookmark");

ASPOSE_ASSERT_EQ(true, customProperty->get_IsLinkToContent());
ASSERT_EQ(u"MyBookmark", customProperty->get_LinkSource());
ASPOSE_ASSERT_EQ(u"Hello world!", customProperty->get_Value());

doc->Save(get_ArtifactsDir() + u"DocumentProperties.LinkCustomDocumentPropertiesToBookmark.docx");
```

## انظر أيضًا

* Class [DocumentProperty](../../documentproperty/)
* Class [CustomDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
