---
title: Fill.Pattern
linktitle: Pattern
articleTitle: Pattern
second_title: Aspose.Words for .NET
description: 探索“填充图案”属性，轻松访问和自定义设计的图案类型。使用独特的填充选项增强您的项目效果！
type: docs
weight: 160
url: /zh/net/aspose.words.drawing/fill/pattern/
---
## Fill.Pattern property

获得[`PatternType`](../../patterntype/)用于填充。

```csharp
public PatternType Pattern { get; }
```

## 例子

展示如何设置形状的图案。

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Fill fill = shape.Fill;

Console.WriteLine("Pattern value is: {0}", fill.Pattern);

// 有几种方法可以指定填充图案。
// 1 - 将图案应用于形状填充：
fill.Patterned(PatternType.DiagonalBrick);

// 2 - 将前景色和背景色的图案应用于形状填充：
fill.Patterned(PatternType.DiagonalBrick, Color.Aqua, Color.Bisque);

doc.Save(ArtifactsDir + "Shape.FillPattern.docx");
```

### 也可以看看

* enum [PatternType](../../patterntype/)
* class [Fill](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
