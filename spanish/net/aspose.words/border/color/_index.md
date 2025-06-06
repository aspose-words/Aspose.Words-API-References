---
title: Border.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words para .NET
description: Personalice sus diseños sin esfuerzo con la propiedad Color del borde, que le permite establecer y modificar los colores del borde para lograr un impacto visual sorprendente.
type: docs
weight: 10
url: /es/net/aspose.words/border/color/
---
## Border.Color property

Obtiene o establece el color del borde.

```csharp
public Color Color { get; set; }
```

## Ejemplos

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

* class [Border](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
