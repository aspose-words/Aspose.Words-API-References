---
title: Fill.BackTintAndShade
linktitle: BackTintAndShade
articleTitle: BackTintAndShade
second_title: Aspose.Words para .NET
description: Ajuste la propiedad BackTintAndShade para aclarar u oscurecer sin esfuerzo el color de fondo, mejorando el atractivo visual de su diseño y la experiencia del usuario.
type: docs
weight: 30
url: /es/net/aspose.words.drawing/fill/backtintandshade/
---
## Fill.BackTintAndShade property

Obtiene o establece un valor doble que aclara u oscurece el color de fondo.

```csharp
public double BackTintAndShade { get; set; }
```

### Excepciones

| excepción | condición |
| --- | --- |
| ArgumentOutOfRangeException | Se lanza si se establece esta propiedad en un valor menor que -1 o mayor que 1. |

## Observaciones

Los valores permitidos están en el rango de -1 (el más oscuro) a 1 (el más claro) para esta propiedad.

Cero (0) es neutral.

## Ejemplos

Muestra cómo establecer el color del tema para el color de la forma de primer plano/fondo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.RoundRectangle, 80, 80);

Fill fill = shape.Fill;
fill.ForeThemeColor = ThemeColor.Dark1;
fill.BackThemeColor = ThemeColor.Background2;

// Nota: no utilice "BackThemeColor" y "BackTintAndShade" para el relleno de fuente.
if (fill.BackTintAndShade == 0)
    fill.BackTintAndShade = 0.2;

doc.Save(ArtifactsDir + "Shape.FillThemeColor.docx");
```

### Ver también

* class [Fill](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
