---
title: Font.Bold
second_title: Referencia de API de Aspose.Words para .NET
description: Font propiedad. Verdadero si la fuente está en negrita.
type: docs
weight: 40
url: /es/net/aspose.words/font/bold/
---
## Font.Bold property

Verdadero si la fuente está en negrita.

```csharp
public bool Bold { get; set; }
```

### Ejemplos

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


