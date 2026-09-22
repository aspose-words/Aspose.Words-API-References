---
title: "Aspose::Words::Properties::DocumentProperty::get_IsLinkToContent metodu"
linktitle: "get_IsLinkToContent"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Properties::DocumentProperty::get_IsLinkToContent metodu. C++'ta bu özelliğin içeriğe bağlı olup olmadığını gösterir."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.properties/documentproperty/get_islinktocontent/
---
## DocumentProperty::get_IsLinkToContent method


Bu özelliğin içeriğe bağlı olup olmadığını gösterir.

```cpp
bool Aspose::Words::Properties::DocumentProperty::get_IsLinkToContent()
```


## Örnekler



Bir özel belge özelliğinin bir yer imine nasıl bağlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartBookmark(u"MyBookmark");
builder->Write(u"Hello world!");
builder->EndBookmark(u"MyBookmark");

// Yeni bir özel özelliği bir yer imine bağlayın. Bu özelliğin değeri
// "LinkSource" üyesinde referans verdiği yer imininin içeriği olacaktır.
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> customProperties = doc->get_CustomDocumentProperties();
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> customProperty = customProperties->AddLinkToContent(u"Bookmark", u"MyBookmark");

ASPOSE_ASSERT_EQ(true, customProperty->get_IsLinkToContent());
ASSERT_EQ(u"MyBookmark", customProperty->get_LinkSource());
ASPOSE_ASSERT_EQ(u"Hello world!", customProperty->get_Value());

doc->Save(get_ArtifactsDir() + u"DocumentProperties.LinkCustomDocumentPropertiesToBookmark.docx");
```

## Ayrıca Bakınız

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
