---
title: Fill.ForeThemeColor
linktitle: ForeThemeColor
articleTitle: ForeThemeColor
second_title: Aspose.Words для .NET
description: Узнайте, как настроить свойство ForeThemeColor, чтобы настроить свой дизайн с помощью ярких цветов заливки. Улучшите визуальную привлекательность вашего проекта без усилий!
type: docs
weight: 80
url: /ru/net/aspose.words.drawing/fill/forethemecolor/
---
## Fill.ForeThemeColor property

Возвращает или задает объект ThemeColor, представляющий цвет переднего плана для заливки.

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
