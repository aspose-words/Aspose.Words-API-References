---
title: Stroke.ForeThemeColor
linktitle: ForeThemeColor
articleTitle: ForeThemeColor
second_title: Aspose.Words para .NET
description: Gestiona fácilmente el color de primer plano de tu trazo con la propiedad Stroke ForeThemeColor. ¡Personaliza tus diseños con vibrantes colores de tema!
type: docs
weight: 140
url: /es/net/aspose.words.drawing/stroke/forethemecolor/
---
## Stroke.ForeThemeColor property

Obtiene o establece un objeto ThemeColor que representa el color de primer plano del trazo.

```csharp
public ThemeColor ForeThemeColor { get; set; }
```

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

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Stroke](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
