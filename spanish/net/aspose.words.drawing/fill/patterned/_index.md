---
title: Fill.Patterned
linktitle: Patterned
articleTitle: Patterned
second_title: Aspose.Words para .NET
description: Descubra el método Fill Patterned para aplicar sin esfuerzo patrones únicos a sus diseños, mejorando la creatividad y el atractivo visual de sus proyectos.
type: docs
weight: 230
url: /es/net/aspose.words.drawing/fill/patterned/
---
## Patterned(*[PatternType](../../patterntype/)*) {#patterned}

Establece el relleno especificado en un patrón.

```csharp
public void Patterned(PatternType patternType)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| patternType | PatternType | [`PatternType`](../../patterntype/) |

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

---

## Patterned(*[PatternType](../../patterntype/), Color, Color*) {#patterned_1}

Establece el relleno especificado en un patrón.

```csharp
public void Patterned(PatternType patternType, Color foreColor, Color backColor)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| patternType | PatternType | [`PatternType`](../../patterntype/) |
| foreColor | Color | El color del relleno del primer plano. |
| backColor | Color | El color del relleno de fondo. |

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
