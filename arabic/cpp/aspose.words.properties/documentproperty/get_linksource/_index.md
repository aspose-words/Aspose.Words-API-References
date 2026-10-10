---
title: "طريقة Aspose::Words::Properties::DocumentProperty::get_LinkSource"
linktitle: "get_LinkSource"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Properties::DocumentProperty::get_LinkSource. يحصل على مصدر خاصية المستند المخصصة المرتبطة في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.properties/documentproperty/get_linksource/
---
## DocumentProperty::get_LinkSource method


يحصل على مصدر خاصية المستند المخصصة المرتبطة.

```cpp
System::String Aspose::Words::Properties::DocumentProperty::get_LinkSource() const
```


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

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
