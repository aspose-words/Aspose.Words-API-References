---
title: "Aspose::Words::Properties::CustomDocumentProperties::AddLinkToContent método"
linktitle: "AddLinkToContent"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Properties::CustomDocumentProperties::AddLinkToContent método. Crea una nueva propiedad de documento personalizada vinculada al contenido en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.properties/customdocumentproperties/addlinktocontent/
---
## CustomDocumentProperties::AddLinkToContent method


Crea una nueva propiedad de documento personalizada vinculada al contenido.

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::CustomDocumentProperties::AddLinkToContent(const System::String &name, const System::String &linkSource)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| name | const System::String\& | El nombre de la propiedad. |
| linkSource | const System::String\& | El origen de la propiedad. |

### ReturnValue

El objeto de propiedad recién creado o **null** cuando el *linkSource* es inválido.

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

* Class [DocumentProperty](../../documentproperty/)
* Class [CustomDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
