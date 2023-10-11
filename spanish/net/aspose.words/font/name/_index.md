---
title: Font.Name
second_title: Referencia de API de Aspose.Words para .NET
description: Font propiedad. Obtiene o establece el nombre de la fuente.
type: docs
weight: 230
url: /es/net/aspose.words/font/name/
---
## Font.Name property

Obtiene o establece el nombre de la fuente.

```csharp
public string Name { get; set; }
```

### Observaciones

Al llegar, regresa[`NameAscii`](../nameascii/).

Al configurar, establece[`NameAscii`](../nameascii/) ,[`NameBi`](../namebi/) ,[`NameFarEast`](../namefareast/) y[`NameOther`](../nameother/) al valor especificado.

### Ejemplos

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

Muestra cómo insertar texto formateado usando DocumentBuilder.

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
* espacio de nombres [Aspose.Words](../../font/)
* asamblea [Aspose.Words](../../../)


