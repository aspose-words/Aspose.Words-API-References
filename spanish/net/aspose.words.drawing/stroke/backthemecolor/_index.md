---
title: Stroke.BackThemeColor
linktitle: BackThemeColor
articleTitle: BackThemeColor
second_title: Aspose.Words para .NET
description: Personaliza tu diseño con la propiedad Stroke BackThemeColor. Define fácilmente un ThemeColor para el fondo de tu trazo y mejora su atractivo visual.
type: docs
weight: 20
url: /es/net/aspose.words.drawing/stroke/backthemecolor/
---
## Stroke.BackThemeColor property

Obtiene o establece un objeto ThemeColor que representa el color de fondo del trazo.

```csharp
public ThemeColor BackThemeColor { get; set; }
```

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

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Stroke](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
