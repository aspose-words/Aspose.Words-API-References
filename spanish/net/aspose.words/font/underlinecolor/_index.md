---
title: Font.UnderlineColor
linktitle: UnderlineColor
articleTitle: UnderlineColor
second_title: Aspose.Words para .NET
description: Descubra la propiedad Font UnderlineColor para personalizar fácilmente el color de subrayado de su fuente para mejorar el estilo del texto y el atractivo visual.
type: docs
weight: 550
url: /es/net/aspose.words/font/underlinecolor/
---
## Font.UnderlineColor property

Obtiene o establece el color del subrayado aplicado a la fuente.

```csharp
public Color UnderlineColor { get; set; }
```

## Ejemplos

Muestra cómo configurar el estilo y el color de un subrayado de texto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Underline = Underline.Dotted;
builder.Font.UnderlineColor = Color.Red;

builder.Writeln("Underlined text.");

doc.Save(ArtifactsDir + "Font.Underlines.docx");
```

### Ver también

* class [Font](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
