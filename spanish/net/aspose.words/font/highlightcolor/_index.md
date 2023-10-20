---
title: Font.HighlightColor
linktitle: HighlightColor
articleTitle: HighlightColor
second_title: Aspose.Words para .NET
description: Font HighlightColor propiedad. Obtiene o establece el color de resaltado marcador en C#.
type: docs
weight: 150
url: /es/net/aspose.words/font/highlightcolor/
---
## Font.HighlightColor property

Obtiene o establece el color de resaltado (marcador).

```csharp
public Color HighlightColor { get; set; }
```

## Ejemplos

Muestra cómo dar formato a una serie de texto usando su propiedad de fuente.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

### Ver también

* class [Font](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
