---
title: ShapeBase.IsTopLevel
linktitle: IsTopLevel
articleTitle: IsTopLevel
second_title: Aspose.Words для .NET
description: Откройте для себя ShapeBase IsTopLevel. Быстро проверяйте, является ли фигура отдельно стоящей, улучшая рабочий процесс проектирования с помощью эффективного управления группами.
type: docs
weight: 370
url: /ru/net/aspose.words.drawing/shapebase/istoplevel/
---
## ShapeBase.IsTopLevel property

Возврат`истинный` если эта фигура не является дочерней по отношению к группе фигур.

```csharp
public bool IsTopLevel { get; }
```

## Примеры

Показывает, как определить, является ли фигура частью групповой фигуры.

```csharp
Document doc = new Document();

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
shape.WrapType = WrapType.None;

// Фигура по умолчанию не является частью какой-либо групповой фигуры, и поэтому ее свойство «IsTopLevel» имеет значение «true».
Assert.True(shape.IsTopLevel);

GroupShape group = new GroupShape(doc);
group.AppendChild(shape);

// После того, как мы ассимилируем фигуру в групповую фигуру, свойство «IsTopLevel» меняется на «false».
Assert.False(shape.IsTopLevel);
```

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
