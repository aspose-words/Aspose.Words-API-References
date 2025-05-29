---
title: Stroke.ForeThemeColor
linktitle: ForeThemeColor
articleTitle: ForeThemeColor
second_title: Aspose.Words для .NET
description: Управляйте цветом переднего плана вашего штриха без усилий с помощью свойства Stroke ForeThemeColor. Настройте свои дизайны с помощью ярких цветов темы!
type: docs
weight: 140
url: /ru/net/aspose.words.drawing/stroke/forethemecolor/
---
## Stroke.ForeThemeColor property

Возвращает или задает объект ThemeColor, представляющий цвет переднего плана обводки.

```csharp
public ThemeColor ForeThemeColor { get; set; }
```

## Примеры

Показывает, как задать цвет, оттенок и тень темы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 100, 40);
Stroke stroke = shape.Stroke;
stroke.ForeThemeColor = ThemeColor.Dark1;
stroke.ForeTintAndShade = 0.5;

doc.Save(ArtifactsDir + "Shape.StrokeForeThemeColors.docx");
```

### Смотрите также

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Stroke](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
