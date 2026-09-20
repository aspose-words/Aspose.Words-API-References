---
title: "Método Aspose::Words::Properties::DocumentProperty::get_LinkSource"
linktitle: "get_LinkSource"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Properties::DocumentProperty::get_LinkSource. Obtiene la fuente de una propiedad de documento personalizada vinculada en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.properties/documentproperty/get_linksource/
---
## DocumentProperty::get_LinkSource method


Obtiene la fuente de una propiedad de documento personalizada vinculada.

```cpp
System::String Aspose::Words::Properties::DocumentProperty::get_LinkSource() const
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
