---
title: "Aspose::Words::Markup::SdtAppearance enum"
linktitle: "SdtAppearance"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Markup::SdtAppearance enum. Especifica la apariencia de una etiqueta de documento estructurado en C++."
type: docs
weight: 18000
url: /es/cpp/aspose.words.markup/sdtappearance/
---
## SdtAppearance enum


Especifica la apariencia de una etiqueta de documento estructurado.

```cpp
enum class SdtAppearance
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| BoundingBox | 0 | Representa una etiqueta de documento estructurado mostrada como un rectángulo sombreado o un cuadro delimitador. |
| Etiquetas | 1 | Representa una etiqueta de documento estructurado mostrada como marcadores de inicio y fin. |
| Oculto | 2 | Representa una etiqueta de documento estructurado que no se muestra. |
| Default | n/a | Predeterminado a [BoundingBox](./). |


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

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
