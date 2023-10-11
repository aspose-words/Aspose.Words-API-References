---
title: ShadowFormat.Clear
second_title: Справочник по API Aspose.Words для .NET
description: ShadowFormat метод. Очищает формат тени.
type: docs
weight: 30
url: /ru/net/aspose.words.drawing/shadowformat/clear/
---
## ShadowFormat.Clear method

Очищает формат тени.

```csharp
public void Clear()
```

### Примеры

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
* пространство имен [Aspose.Words.Drawing](../../shadowformat/)
* сборка [Aspose.Words](../../../)


