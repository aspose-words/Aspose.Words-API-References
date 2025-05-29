---
title: FindReplaceOptions.IgnoreShapes
linktitle: IgnoreShapes
articleTitle: IgnoreShapes
second_title: Aspose.Words для .NET
description: Откройте для себя свойство IgnoreShapes FindReplaceOptions. Управляйте включением фигур в обработку текста с помощью этого важного логического параметра для повышения точности.
type: docs
weight: 110
url: /ru/net/aspose.words.replacing/findreplaceoptions/ignoreshapes/
---
## FindReplaceOptions.IgnoreShapes property

Возвращает или задает логическое значение, указывающее, следует ли игнорировать фигуры в тексте.

Значение по умолчанию:`ЛОЖЬ`.

```csharp
public bool IgnoreShapes { get; set; }
```

## Примеры

Показывает, как игнорировать фигуры при замене текста.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertShape(ShapeType.Balloon, 200, 200);
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

FindReplaceOptions findReplaceOptions = new FindReplaceOptions() { IgnoreShapes = true };
builder.Document.Range.Replace("Lorem ipsum dolor sit amet, consectetur adipiscing elit.Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
    "Lorem ipsum dolor sit amet, consectetur adipiscing elit.", findReplaceOptions);
Assert.AreEqual("Lorem ipsum dolor sit amet, consectetur adipiscing elit.", builder.Document.GetText().Trim());
```

### Смотрите также

* class [FindReplaceOptions](../)
* пространство имен [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* сборка [Aspose.Words](../../../)
