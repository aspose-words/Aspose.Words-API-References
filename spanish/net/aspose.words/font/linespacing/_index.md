---
title: Font.LineSpacing
linktitle: LineSpacing
articleTitle: LineSpacing
second_title: Aspose.Words para .NET
description: Descubra la propiedad Font LineSpacing, que proporciona el espaciado de línea preciso en puntos, mejorando la legibilidad y el diseño de su texto.
type: docs
weight: 190
url: /es/net/aspose.words/font/linespacing/
---
## Font.LineSpacing property

Devuelve el espacio entre líneas de esta fuente (en puntos).

```csharp
public double LineSpacing { get; }
```

## Ejemplos

Muestra cómo obtener el espacio entre líneas de una fuente, en puntos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Establezca diferentes fuentes para DocumentBuilder y verifique su espacio entre líneas.
builder.Font.Name = "Calibri";
Assert.AreEqual(14.6484375d, builder.Font.LineSpacing);

builder.Font.Name = "Times New Roman";
Assert.AreEqual(13.798828125d, builder.Font.LineSpacing);
```

### Ver también

* class [Font](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
