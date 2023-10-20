---
title: ShadowFormat.Visible
linktitle: Visible
articleTitle: Visible
second_title: Aspose.Words для .NET
description: ShadowFormat Visible свойство. Возвращаетистинный если форматирование примененное к этому экземпляру видимо на С#.
type: docs
weight: 20
url: /ru/net/aspose.words.drawing/shadowformat/visible/
---
## ShadowFormat.Visible property

Возвращает`истинный` если форматирование, примененное к этому экземпляру, видимо.

```csharp
public bool Visible { get; }
```

## Примечания

В отличие от[`Clear`](../clear/) , назначение`ЛОЖЬ` to Visible не очищает форматирование, он только скрывает эффект формы.

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
