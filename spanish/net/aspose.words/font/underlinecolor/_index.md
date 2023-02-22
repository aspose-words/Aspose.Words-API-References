---
title: Font.UnderlineColor
second_title: Referencia de API de Aspose.Words para .NET
description: Font propiedad. Obtiene o establece el color del subrayado aplicado a la fuente.
type: docs
weight: 540
url: /es/net/aspose.words/font/underlinecolor/
---
## Font.UnderlineColor property

Obtiene o establece el color del subrayado aplicado a la fuente.

```csharp
public Color UnderlineColor { get; set; }
```

### Ejemplos

Muestra cómo configurar el estilo y el color de un texto subrayado.

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
* espacio de nombres [Aspose.Words](../../font/)
* asamblea [Aspose.Words](../../../)


