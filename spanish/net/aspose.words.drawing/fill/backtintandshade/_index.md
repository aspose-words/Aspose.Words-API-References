---
title: Fill.BackTintAndShade
linktitle: BackTintAndShade
articleTitle: BackTintAndShade
second_title: Aspose.Words para .NET
description: Fill BackTintAndShade propiedad. Obtiene o establece un valor doble que aclara u oscurece el color de fondo en C#.
type: docs
weight: 30
url: /es/net/aspose.words.drawing/fill/backtintandshade/
---
## Fill.BackTintAndShade property

Obtiene o establece un valor doble que aclara u oscurece el color de fondo.

```csharp
public double BackTintAndShade { get; set; }
```

## Observaciones

Los valores permitidos están dentro del rango de -1 (el más oscuro) a 1 (el más claro) para esta propiedad. Cero (0) es neutral. Intentar establecer esta propiedad en un valor inferior a -1 o superior a 1 da como resultadoArgumentOutOfRangeException.

## Ejemplos

Muestra cómo configurar el color del tema para el color de la forma de primer plano/fondo.

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
