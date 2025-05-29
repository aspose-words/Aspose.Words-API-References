---
title: ShapeBase.MarkupLanguage
linktitle: MarkupLanguage
articleTitle: MarkupLanguage
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ShapeBase MarkupLanguage для улучшенного управления графическими объектами. Откройте для себя бесшовную интеграцию и улучшенную эффективность дизайна уже сегодня!
type: docs
weight: 410
url: /ru/net/aspose.words.drawing/shapebase/markuplanguage/
---
## ShapeBase.MarkupLanguage property

Получает MarkupLanguage, используемый для этого графического объекта.

```csharp
public ShapeMarkupLanguage MarkupLanguage { get; }
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

* enum [ShapeMarkupLanguage](../../shapemarkuplanguage/)
* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
