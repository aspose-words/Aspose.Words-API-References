---
title: Stroke.BackTintAndShade
linktitle: BackTintAndShade
articleTitle: BackTintAndShade
second_title: Aspose.Words для .NET
description: Легко настройте цвет фона обводки с помощью Stroke BackTintAndShade. Контролируйте яркость и темноту для идеального завершения дизайна.
type: docs
weight: 30
url: /ru/net/aspose.words.drawing/stroke/backtintandshade/
---
## Stroke.BackTintAndShade property

Возвращает или задает двойное значение, которое осветляет или затемняет цвет фона обводки.

```csharp
public double BackTintAndShade { get; set; }
```

## Примечания

Допустимые значения для этого свойства находятся в диапазоне от -1 (самый темный) до 1 (самый светлый). Ноль (0) нейтрален. Попытка установить это свойство на значение меньше -1 или больше 1 приводит кArgumentOutOfRangeException.

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

* class [Stroke](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
