---
title: Fill.Pattern
linktitle: Pattern
articleTitle: Pattern
second_title: Aspose.Words para .NET
description: Descubre la propiedad Patrón de relleno para acceder y personalizar fácilmente el Tipo de patrón en tus diseños. ¡Mejora tus proyectos con opciones de relleno únicas!
type: docs
weight: 160
url: /es/net/aspose.words.drawing/fill/pattern/
---
## Fill.Pattern property

Obtiene un[`PatternType`](../../patterntype/) para el relleno.

```csharp
public PatternType Pattern { get; }
```

## Ejemplos

Muestra cómo establecer un patrón para una forma.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Fill fill = shape.Fill;

Console.WriteLine("Pattern value is: {0}", fill.Pattern);

//Hay varias formas de rellenar un patrón especificado.
// 1 - Aplicar patrón al relleno de forma:
fill.Patterned(PatternType.DiagonalBrick);

// 2 - Aplicar patrón con colores de primer plano y de fondo al relleno de la forma:
fill.Patterned(PatternType.DiagonalBrick, Color.Aqua, Color.Bisque);

doc.Save(ArtifactsDir + "Shape.FillPattern.docx");
```

### Ver también

* enum [PatternType](../../patterntype/)
* class [Fill](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
