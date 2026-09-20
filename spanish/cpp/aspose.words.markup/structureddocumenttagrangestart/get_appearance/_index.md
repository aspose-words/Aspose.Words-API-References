---
title: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Appearance método"
linktitle: "get_Appearance"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Appearance método. Obtiene o establece la apariencia de la etiqueta de documento estructurado en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.markup/structureddocumenttagrangestart/get_appearance/
---
## StructuredDocumentTagRangeStart::get_Appearance method


Obtiene o establece la apariencia de la etiqueta de documento estructurado.

```cpp
Aspose::Words::Markup::SdtAppearance Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Appearance() override
```


## Ejemplos



Muestra cómo mostrar la etiqueta alrededor del contenido.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");
auto tag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, 0, true));

if (tag->get_Appearance() == Aspose::Words::Markup::SdtAppearance::Hidden)
{
    tag->set_Appearance(Aspose::Words::Markup::SdtAppearance::Tags);
}
```

## Ver también

* Enum [SdtAppearance](../../sdtappearance/)
* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
