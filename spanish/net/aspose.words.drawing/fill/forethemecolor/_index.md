---
title: Fill.ForeThemeColor
linktitle: ForeThemeColor
articleTitle: ForeThemeColor
second_title: Aspose.Words para .NET
description: Descubre cómo configurar la propiedad ForeThemeColor para personalizar tu diseño con colores de relleno vibrantes. ¡Mejora el atractivo visual de tu proyecto sin esfuerzo!
type: docs
weight: 80
url: /es/net/aspose.words.drawing/fill/forethemecolor/
---
## Fill.ForeThemeColor property

Obtiene o establece un objeto ThemeColor que representa el color de primer plano para el relleno.

```csharp
public ThemeColor ForeThemeColor { get; set; }
```

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

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Fill](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
