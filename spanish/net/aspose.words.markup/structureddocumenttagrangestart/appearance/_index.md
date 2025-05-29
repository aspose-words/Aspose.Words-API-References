---
title: StructuredDocumentTagRangeStart.Appearance
linktitle: Appearance
articleTitle: Appearance
second_title: Aspose.Words para .NET
description: Descubra cómo personalizar la apariencia de StructuredDocumentTagRangeStart para mejorar el formato del documento y la legibilidad.
type: docs
weight: 20
url: /es/net/aspose.words.markup/structureddocumenttagrangestart/appearance/
---
## StructuredDocumentTagRangeStart.Appearance property

Obtiene o establece la apariencia de la etiqueta del documento estructurado.

```csharp
public SdtAppearance Appearance { get; set; }
```

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

* enum [SdtAppearance](../../sdtappearance/)
* class [StructuredDocumentTagRangeStart](../)
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)
