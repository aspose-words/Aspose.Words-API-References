---
title: "Método Aspose::Words::Markup::XmlMapping::get_StoreItemId"
linktitle: "get_StoreItemId"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Markup::XmlMapping::get_StoreItemId. Especifica el identificador de datos XML personalizado para la parte de datos XML personalizada que se utilizará para evaluar la expresión XPath en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.markup/xmlmapping/get_storeitemid/
---
## XmlMapping::get_StoreItemId method


Especifica el identificador de datos XML personalizado para la parte de datos XML personalizada que se utilizará para evaluar la expresión [XPath](../get_xpath/).

```cpp
System::String Aspose::Words::Markup::XmlMapping::get_StoreItemId()
```


## Ejemplos



Muestra cómo obtener el identificador de datos XML personalizado de una parte XML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom XML part in structured document tag.docx");

// Las etiquetas de documento estructurado tienen IDs en forma de GUIDs.
auto tag = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTag, 0, true));

ASSERT_EQ(u"{F3029283-4FF8-4DD2-9F31-395F19ACEE85}", tag->get_XmlMapping()->get_StoreItemId());
```

## Ver también

* Class [XmlMapping](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
