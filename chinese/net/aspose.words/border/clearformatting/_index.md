---
title: Border.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words for .NET
description: 使用 Border ClearFormatting 方法将边框属性重置为默认值。简化您的设计流程，提升项目外观！
type: docs
weight: 90
url: /zh/net/aspose.words/border/clearformatting/
---
## Border.ClearFormatting method

将边框属性重置为默认值。

```csharp
public void ClearFormatting()
```

## 评论

当边框属性重置为默认值时，边框不可见。

## 例子

展示如何删除段落的边框。

```csharp
Document doc = new Document(MyDir + "Borders.docx");

// 每个段落都有一组单独的边框。
// 我们可以通过段落格式对象访问这些边框的外观设置。
BorderCollection borders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;

Assert.AreEqual(Color.Red.ToArgb(), borders[0].Color.ToArgb());
Assert.AreEqual(3.0d, borders[0].LineWidth);
Assert.AreEqual(LineStyle.Single, borders[0].LineStyle);
Assert.True(borders[0].IsVisible);

 // 我们可以通过运行 ClearFormatting 方法立即删除边框。
// 在段落的每个边框上运行此方法将删除其所有边框。
foreach (Border border in borders)
    border.ClearFormatting();

Assert.AreEqual(Color.Empty.ToArgb(), borders[0].Color.ToArgb());
Assert.AreEqual(0.0d, borders[0].LineWidth);
Assert.AreEqual(LineStyle.None, borders[0].LineStyle);
Assert.IsFalse(borders[0].IsVisible);

doc.Save(ArtifactsDir + "Border.ClearFormatting.docx");
```

### 也可以看看

* class [Border](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
