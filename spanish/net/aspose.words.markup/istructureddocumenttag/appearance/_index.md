---
title: IStructuredDocumentTag.Appearance
linktitle: Appearance
articleTitle: Appearance
second_title: Aspose.Words para .NET
description: Descubra la propiedad Apariencia IStructuredDocumentTag para personalizar y mejorar sus etiquetas de documentos estructurados para una mejor experiencia del usuario.
type: docs
weight: 10
url: /es/net/aspose.words.markup/istructureddocumenttag/appearance/
---
## IStructuredDocumentTag.Appearance property

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
* interface [IStructuredDocumentTag](../)
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)
