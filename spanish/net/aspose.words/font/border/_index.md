---
title: Font.Border
second_title: Referencia de API de Aspose.Words para .NET
description: Font propiedad. Devuelve unBorder objeto que especifica el borde de la fuente.
type: docs
weight: 60
url: /es/net/aspose.words/font/border/
---
## Font.Border property

Devuelve un[`Border`](../../border/) objeto que especifica el borde de la fuente.

```csharp
public Border Border { get; }
```

### Ejemplos

Muestra cómo insertar una cadena rodeada por un borde en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

### Ver también

* class [Border](../../border/)
* class [Font](../)
* espacio de nombres [Aspose.Words](../../font/)
* asamblea [Aspose.Words](../../../)


