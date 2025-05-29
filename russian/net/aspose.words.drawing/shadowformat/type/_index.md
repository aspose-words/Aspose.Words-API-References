---
title: ShadowFormat.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words для .NET
description: Изучите свойство ShadowFormat Type, чтобы легко настроить эффекты тени. Получите или установите ShadowType для повышения гибкости дизайна.
type: docs
weight: 20
url: /ru/net/aspose.words.drawing/shadowformat/type/
---
## ShadowFormat.Type property

Получает или задает указанный[`ShadowType`](../../shadowtype/) для ShadowFormat.

```csharp
public ShadowType Type { get; set; }
```

## Примеры

Показывает, как получить цвет тени.

```csharp
Document doc = new Document(MyDir + "Shadow color.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ShadowFormat shadowFormat = shape.ShadowFormat;

Assert.AreEqual(Color.Red.ToArgb(), shadowFormat.Color.ToArgb());
Assert.AreEqual(ShadowType.ShadowMixed, shadowFormat.Type);
```

### Смотрите также

* enum [ShadowType](../../shadowtype/)
* class [ShadowFormat](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
