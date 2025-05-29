---
title: Stroke.ForeTintAndShade
linktitle: ForeTintAndShade
articleTitle: ForeTintAndShade
second_title: Aspose.Words para .NET
description: Ajuste la propiedad Stroke ForeTintAndShade para aclarar u oscurecer sin esfuerzo el color de primer plano de su trazo para un impacto visual mejorado.
type: docs
weight: 150
url: /es/net/aspose.words.drawing/stroke/foretintandshade/
---
## Stroke.ForeTintAndShade property

Obtiene o establece un valor doble que aclara u oscurece el color de primer plano del trazo.

```csharp
public double ForeTintAndShade { get; set; }
```

## Observaciones

Los valores permitidos para esta propiedad están en el rango de -1 (el más oscuro) a 1 (el más claro). El cero (0) es neutro. Intentar establecer esta propiedad en un valor menor que -1 o mayor que 1 resulta enArgumentOutOfRangeException.

## Ejemplos

Muestra cómo establecer el color, el tono y la sombra del tema.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 100, 40);
Stroke stroke = shape.Stroke;
stroke.ForeThemeColor = ThemeColor.Dark1;
stroke.ForeTintAndShade = 0.5;

doc.Save(ArtifactsDir + "Shape.StrokeForeThemeColors.docx");
```

### Ver también

* class [Stroke](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
