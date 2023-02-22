---
title: Font.Size
second_title: Referencia de API de Aspose.Words para .NET
description: Font propiedad. Obtiene o establece el tamaño de fuente en puntos.
type: docs
weight: 340
url: /es/net/aspose.words/font/size/
---
## Font.Size property

Obtiene o establece el tamaño de fuente en puntos.

```csharp
public double Size { get; set; }
```

### Ejemplos

Muestra cómo dar formato a una tirada de texto utilizando su propiedad de fuente.

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

Muestra cómo insertar texto con formato utilizando DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Especifique el formato de fuente, luego agregue texto.
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
* espacio de nombres [Aspose.Words](../../font/)
* asamblea [Aspose.Words](../../../)


