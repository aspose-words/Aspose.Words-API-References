---
title: Stroke.BackThemeColor
linktitle: BackThemeColor
articleTitle: BackThemeColor
second_title: Aspose.Words для .NET
description: Настройте свой дизайн с помощью свойства Stroke BackThemeColor. Легко установите ThemeColor для фона вашего штриха, чтобы улучшить визуальную привлекательность.
type: docs
weight: 20
url: /ru/net/aspose.words.drawing/stroke/backthemecolor/
---
## Stroke.BackThemeColor property

Возвращает или задает объект ThemeColor, представляющий цвет фона обводки.

```csharp
public ThemeColor BackThemeColor { get; set; }
```

## Примеры

Показывает, как восстановить цвет, оттенок и тень темы.

```csharp
Document doc = new Document(MyDir + "Stroke gradient outline.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Stroke stroke = shape.Stroke;
stroke.BackThemeColor = ThemeColor.Dark2;
stroke.BackTintAndShade = 0.2d;

doc.Save(ArtifactsDir + "Shape.StrokeBackThemeColors.docx");
```

### Смотрите также

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Stroke](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
