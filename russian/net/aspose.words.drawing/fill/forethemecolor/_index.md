---
title: Fill.ForeThemeColor
linktitle: ForeThemeColor
articleTitle: ForeThemeColor
second_title: Aspose.Words для .NET
description: Fill ForeThemeColor свойство. Получает или задает объект ThemeColor который представляет цвет переднего плана для заливки на С#.
type: docs
weight: 70
url: /ru/net/aspose.words.drawing/fill/forethemecolor/
---
## Fill.ForeThemeColor property

Получает или задает объект ThemeColor, который представляет цвет переднего плана для заливки.

```csharp
public ThemeColor ForeThemeColor { get; set; }
```

## Примеры

Показывает, как установить цвет темы для цвета фигуры переднего плана/фона.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.RoundRectangle, 80, 80);

Fill fill = shape.Fill;
fill.ForeThemeColor = ThemeColor.Dark1;
fill.BackThemeColor = ThemeColor.Background2;

// Примечание: не используйте «BackThemeColor» и «BackTintAndShade» для заливки шрифта.
if (fill.BackTintAndShade == 0)
    fill.BackTintAndShade = 0.2;

doc.Save(ArtifactsDir + "Shape.FillThemeColor.docx");
```

### Смотрите также

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Fill](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
