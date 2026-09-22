---
title: "Aspose::Words::Properties::CustomDocumentProperties::AddLinkToContent method"
linktitle: "AddLinkToContent"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Properties::CustomDocumentProperties::AddLinkToContent yöntemi. C++'ta içeriğe bağlı yeni bir özel belge özelliği oluşturur."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.properties/customdocumentproperties/addlinktocontent/
---
## CustomDocumentProperties::AddLinkToContent method


İçeriğe bağlı yeni bir özel belge özelliği oluşturur.

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::CustomDocumentProperties::AddLinkToContent(const System::String &name, const System::String &linkSource)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | const System::String\& | Özelliğin adı. |
| linkSource | const System::String\& | Özelliğin kaynağı. |

### ReturnValue

Yeni oluşturulan özelliğin nesnesi veya *linkSource* geçersiz olduğunda **null**.

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

* Class [DocumentProperty](../../documentproperty/)
* Class [CustomDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
