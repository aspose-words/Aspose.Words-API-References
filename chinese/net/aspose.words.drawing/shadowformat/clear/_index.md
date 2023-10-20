---
title: ShadowFormat.Clear
linktitle: Clear
articleTitle: Clear
second_title: 用于 .NET 的 Aspose.Words
description: ShadowFormat Clear 方法. 清除阴影格式 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words.drawing/shadowformat/clear/
---
## ShadowFormat.Clear method

清除阴影格式。

```csharp
public void Clear()
```

## 例子

展示如何使用形状的阴影格式。

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];

if (shape.ShadowFormat.Visible && shape.ShadowFormat.Type == ShadowType.Shadow2)                
    shape.ShadowFormat.Type = ShadowType.Shadow7;

if (shape.ShadowFormat.Type == ShadowType.ShadowMixed)            
    shape.ShadowFormat.Clear();
```

### 也可以看看

* class [ShadowFormat](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
