---
title: SdtAppearance Enum
linktitle: SdtAppearance
articleTitle: SdtAppearance
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Markup.SdtAppearance para personalizar la apariencia de las etiquetas de documentos estructurados. ¡Mejore el formato de sus documentos sin esfuerzo!
type: docs
weight: 4680
url: /es/net/aspose.words.markup/sdtappearance/
---
## SdtAppearance enumeration

Especifica la apariencia de una etiqueta de documento estructurado.

```csharp
public enum SdtAppearance
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| BoundingBox | `0` | Representa una etiqueta de documento estructurada que se muestra como un rectángulo sombreado o un cuadro delimitador. |
| Tags | `1` | Representa una etiqueta de documento estructurada que se muestra como marcadores de inicio y fin. |
| Hidden | `2` | Representa una etiqueta de documento estructurado que no se muestra. |
| Default | `0` | El valor predeterminado esBoundingBox . |

## Ejemplos

Muestra cómo mostrar etiquetas alrededor del contenido.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");
StructuredDocumentTagRangeStart tag =
    doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true) as StructuredDocumentTagRangeStart;

if (tag.Appearance == SdtAppearance.Hidden)
    tag.Appearance = SdtAppearance.Tags;
```

### Ver también

* espacio de nombres [Aspose.Words.Markup](../../aspose.words.markup/)
* asamblea [Aspose.Words](../../)
