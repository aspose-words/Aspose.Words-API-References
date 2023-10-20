---
title: Font.LineSpacing
linktitle: LineSpacing
articleTitle: LineSpacing
second_title: Aspose.Words para .NET
description: Font LineSpacing propiedad. Devuelve el interlineado de esta fuente en puntos en C#.
type: docs
weight: 190
url: /es/net/aspose.words/font/linespacing/
---
## Font.LineSpacing property

Devuelve el interlineado de esta fuente (en puntos).

```csharp
public double LineSpacing { get; }
```

## Ejemplos

Muestra cómo obtener el interlineado de una fuente, en puntos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Establece diferentes fuentes para DocumentBuilder y verifica su interlineado.
builder.Font.Name = "Calibri";
Assert.AreEqual(14.6484375d, builder.Font.LineSpacing);

builder.Font.Name = "Times New Roman";
Assert.AreEqual(13.798828125d, builder.Font.LineSpacing);
```

### Ver también

* class [Font](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
