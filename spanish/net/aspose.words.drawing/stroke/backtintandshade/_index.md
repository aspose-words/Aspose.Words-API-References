---
title: Stroke.BackTintAndShade
linktitle: BackTintAndShade
articleTitle: BackTintAndShade
second_title: Aspose.Words para .NET
description: Ajusta fácilmente el color de fondo de tu trazo con Stroke BackTintAndShade. Controla la claridad y la oscuridad para un acabado de diseño perfecto.
type: docs
weight: 30
url: /es/net/aspose.words.drawing/stroke/backtintandshade/
---
## Stroke.BackTintAndShade property

Obtiene o establece un valor doble que aclara u oscurece el color de fondo del trazo.

```csharp
public double BackTintAndShade { get; set; }
```

## Observaciones

Los valores permitidos para esta propiedad están en el rango de -1 (el más oscuro) a 1 (el más claro). El cero (0) es neutro. Intentar establecer esta propiedad en un valor menor que -1 o mayor que 1 resulta enArgumentOutOfRangeException.

## Ejemplos

Muestra cómo restablecer el color, el tono y la sombra del tema.

```csharp
Document doc = new Document(MyDir + "Stroke gradient outline.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Stroke stroke = shape.Stroke;
stroke.BackThemeColor = ThemeColor.Dark2;
stroke.BackTintAndShade = 0.2d;

doc.Save(ArtifactsDir + "Shape.StrokeBackThemeColors.docx");
```

### Ver también

* class [Stroke](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
