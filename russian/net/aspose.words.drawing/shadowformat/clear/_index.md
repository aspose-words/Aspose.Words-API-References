---
title: ShadowFormat.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words для .NET
description: ShadowFormat Clear метод. Очищает формат тени на С#.
type: docs
weight: 30
url: /ru/net/aspose.words.drawing/shadowformat/clear/
---
## ShadowFormat.Clear method

Очищает формат тени.

```csharp
public void Clear()
```

## Примеры

Показывает, как работать с форматированием тени для фигуры.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];

if (shape.ShadowFormat.Visible && shape.ShadowFormat.Type == ShadowType.Shadow2)                
    shape.ShadowFormat.Type = ShadowType.Shadow7;

if (shape.ShadowFormat.Type == ShadowType.ShadowMixed)            
    shape.ShadowFormat.Clear();
```

### Смотрите также

* class [ShadowFormat](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
