---
title: ShapeBase.Hidden
linktitle: Hidden
articleTitle: Hidden
second_title: Aspose.Words для .NET
description: Управляйте видимостью формы с помощью скрытого свойства ShapeBase. Легко переключайтесь между видимым и скрытым для повышения гибкости дизайна.
type: docs
weight: 230
url: /ru/net/aspose.words.drawing/shapebase/hidden/
---
## ShapeBase.Hidden property

Возвращает или задает логическое значение, указывающее, видна ли фигура.

```csharp
public bool Hidden { get; set; }
```

## Примечания

Значение по умолчанию:`ЛОЖЬ` .

## Примеры

Показывает, как скрыть фигуру.

```csharp
Document doc = new Document(MyDir + "Shadow color.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
if (!shape.Hidden)
    shape.Hidden = true;

doc.Save(ArtifactsDir + "Shape.Hidden.docx");
```

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
