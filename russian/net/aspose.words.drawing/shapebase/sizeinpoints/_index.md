---
title: ShapeBase.SizeInPoints
linktitle: SizeInPoints
articleTitle: SizeInPoints
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ShapeBase SizeInPoints, позволяющее легко извлекать и управлять размерами фигур в точках для точного управления проектом.
type: docs
weight: 540
url: /ru/net/aspose.words.drawing/shapebase/sizeinpoints/
---
## ShapeBase.SizeInPoints property

Получает размер фигуры в точках.

```csharp
public SizeF SizeInPoints { get; }
```

## Примеры

Показывает, как проверить размер фигуры и язык разметки.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Dml, shape.MarkupLanguage);
Assert.AreEqual(new SizeF(300, 300), shape.SizeInPoints);
```

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
