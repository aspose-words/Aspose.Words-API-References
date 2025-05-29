---
title: Font.Size
linktitle: Size
articleTitle: Size
second_title: Aspose.Words para .NET
description: Ajuste fácilmente el tamaño de la fuente con la propiedad Tamaño de fuente. Personalice su texto en puntos para mejorar la legibilidad y el atractivo del diseño.
type: docs
weight: 350
url: /es/net/aspose.words/font/size/
---
## Font.Size property

Obtiene o establece el tamaño de fuente en puntos.

```csharp
public double Size { get; set; }
```

## Ejemplos

Muestra cómo formatear una serie de texto utilizando su propiedad de fuente.

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

Muestra cómo insertar texto formateado utilizando DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Especifique el formato de fuente y luego agregue texto.
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

### Ver también

* class [Font](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
