---
title: BorderCollection.Equals
second_title: Aspose.Words for .NET API 参考
description: BorderCollection 方法. 比较边框的集合
type: docs
weight: 150
url: /zh/net/aspose.words/bordercollection/equals/
---
## BorderCollection.Equals method

比较边框的集合。

```csharp
public bool Equals(BorderCollection brColl)
```

### 例子

显示边框集合如何共享元素。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Write("Paragraph 2.");

// 因为我们在创建时使用了相同的边框配置
// 这些段落，它们的边框集合共享相同的元素。
BorderCollection firstParagraphBorders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;
BorderCollection secondParagraphBorders = builder.CurrentParagraph.ParagraphFormat.Borders;

for (int i = 0; i < firstParagraphBorders.Count; i++)
{
    Assert.IsTrue(firstParagraphBorders[i].Equals(secondParagraphBorders[i]));
    Assert.AreEqual(firstParagraphBorders[i].GetHashCode(), secondParagraphBorders[i].GetHashCode());
    Assert.False(firstParagraphBorders[i].IsVisible);
}

foreach (Border border in secondParagraphBorders)
    border.LineStyle = LineStyle.DotDash;

// 仅在第二段更改边框的线条样式后，
// 边框集合不再共享相同的元素。
for (int i = 0; i < firstParagraphBorders.Count; i++)
{
    Assert.IsFalse(firstParagraphBorders[i].Equals(secondParagraphBorders[i]));
    Assert.AreNotEqual(firstParagraphBorders[i].GetHashCode(), secondParagraphBorders[i].GetHashCode());

    // 更改空边框的外观使其可见。
    Assert.True(secondParagraphBorders[i].IsVisible);
}

doc.Save(ArtifactsDir + "Border.SharedElements.docx");
```

### 也可以看看

* class [BorderCollection](../)
* 命名空间 [Aspose.Words](../../bordercollection/)
* 部件 [Aspose.Words](../../../)


