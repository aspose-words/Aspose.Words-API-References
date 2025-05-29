---
title: Font.Bold
linktitle: Bold
articleTitle: Bold
second_title: Aspose.Words para .NET
description: Descubra la propiedad Font Bold, identifique fácilmente si su texto está en negrita, mejorando la legibilidad y el estilo de sus proyectos de diseño web.
type: docs
weight: 40
url: /es/net/aspose.words/font/bold/
---
## Font.Bold property

Verdadero si la fuente está formateada en negrita.

```csharp
public bool Bold { get; set; }
```

## Ejemplos

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
