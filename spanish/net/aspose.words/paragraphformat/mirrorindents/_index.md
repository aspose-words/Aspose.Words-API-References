---
title: ParagraphFormat.MirrorIndents
linktitle: MirrorIndents
articleTitle: MirrorIndents
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad ParagraphFormat MirrorIndents mejora el formato de su documento al garantizar sangrías izquierda y derecha consistentes para una apariencia pulida.
type: docs
weight: 240
url: /es/net/aspose.words/paragraphformat/mirrorindents/
---
## ParagraphFormat.MirrorIndents property

Obtiene o establece un indicador que indica si las sangrías izquierda y derecha tienen el mismo ancho.

```csharp
public bool MirrorIndents { get; set; }
```

## Ejemplos

Muestra cómo hacer que las sangrías izquierda y derecha sean iguales.

```csharp
Document doc = new Document(MyDir + "Document.docx");
ParagraphFormat format = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat;

format.MirrorIndents = true;

doc.Save(ArtifactsDir + "ParagraphFormat.MirrorIndents.docx");
```

### Ver también

* class [ParagraphFormat](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
