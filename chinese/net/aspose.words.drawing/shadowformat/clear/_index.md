---
title: ShadowFormat.Clear
second_title: Aspose.Words for .NET API 参考
description: ShadowFormat 方法. 清除阴影格式
type: docs
weight: 30
url: /zh/net/aspose.words.drawing/shadowformat/clear/
---
## ShadowFormat.Clear method

清除阴影格式。

```csharp
public void Clear()
```

### 例子

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
* 命名空间 [Aspose.Words.Drawing](../../shadowformat/)
* 部件 [Aspose.Words](../../../)


