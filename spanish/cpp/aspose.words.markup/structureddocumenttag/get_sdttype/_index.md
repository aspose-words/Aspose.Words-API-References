---
title: "Método Aspose::Words::Markup::StructuredDocumentTag::get_SdtType"
linktitle: "get_SdtType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Markup::StructuredDocumentTag::get_SdtType. Obtiene el tipo de esta etiqueta de documento estructurado en C++."
type: docs
weight: 28000
url: /es/cpp/aspose.words.markup/structureddocumenttag/get_sdttype/
---
## StructuredDocumentTag::get_SdtType method


Obtiene el tipo de esta **Structured document tag**.

```cpp
Aspose::Words::Markup::SdtType Aspose::Words::Markup::StructuredDocumentTag::get_SdtType() override
```


## Ejemplos



Muestra cómo obtener el tipo de una etiqueta de documento estructurado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

System::SharedPtr<System::Collections::Generic::List<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>> tags = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> >()->LINQ_ToList();

ASSERT_EQ(Aspose::Words::Markup::SdtType::RepeatingSection, tags->idx_get(0)->get_SdtType());
ASSERT_EQ(Aspose::Words::Markup::SdtType::RepeatingSectionItem, tags->idx_get(1)->get_SdtType());
ASSERT_EQ(Aspose::Words::Markup::SdtType::RichText, tags->idx_get(2)->get_SdtType());
```

## Ver también

* Enum [SdtType](../../sdttype/)
* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
