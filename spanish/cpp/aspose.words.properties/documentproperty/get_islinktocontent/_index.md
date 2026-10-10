---
title: "Aspose::Words::Properties::DocumentProperty::get_IsLinkToContent método"
linktitle: "get_IsLinkToContent"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Properties::DocumentProperty::get_IsLinkToContent método. Muestra si esta propiedad está vinculada al contenido o no en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.properties/documentproperty/get_islinktocontent/
---
## DocumentProperty::get_IsLinkToContent method


Muestra si esta propiedad está vinculada al contenido o no.

```cpp
bool Aspose::Words::Properties::DocumentProperty::get_IsLinkToContent()
```


## Ejemplos



Muestra cómo vincular una propiedad de documento personalizada a un marcador.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartBookmark(u"MyBookmark");
builder->Write(u"Hello world!");
builder->EndBookmark(u"MyBookmark");

// Vincula una nueva propiedad personalizada a un marcador. El valor de esta propiedad
// será el contenido del marcador que referencia en el miembro "LinkSource".
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> customProperties = doc->get_CustomDocumentProperties();
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> customProperty = customProperties->AddLinkToContent(u"Bookmark", u"MyBookmark");

ASPOSE_ASSERT_EQ(true, customProperty->get_IsLinkToContent());
ASSERT_EQ(u"MyBookmark", customProperty->get_LinkSource());
ASPOSE_ASSERT_EQ(u"Hello world!", customProperty->get_Value());

doc->Save(get_ArtifactsDir() + u"DocumentProperties.LinkCustomDocumentPropertiesToBookmark.docx");
```

## Ver también

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
