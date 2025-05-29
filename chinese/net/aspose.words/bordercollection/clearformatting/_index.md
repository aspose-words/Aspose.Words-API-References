---
title: BorderCollection.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words for .NET
description: 了解 BorderCollection ClearFormatting 方法如何轻松删除所有对象边框，以干净、清晰的视觉效果增强您的设计。
type: docs
weight: 140
url: /zh/net/aspose.words/bordercollection/clearformatting/
---
## BorderCollection.ClearFormatting method

删除对象的所有边框。

```csharp
public void ClearFormatting()
```

## 例子

展示如何删除文档中所有段落的所有边框。

```csharp
Document doc = new Document(MyDir + "Borders.docx");

// 在这些设置下，本文档的第一段具有可见的边框。
BorderCollection firstParagraphBorders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;

Assert.AreEqual(Color.Red.ToArgb(), firstParagraphBorders.Color.ToArgb());
Assert.AreEqual(LineStyle.Single, firstParagraphBorders.LineStyle);
Assert.AreEqual(3.0d, firstParagraphBorders.LineWidth);

// 在每个段落上使用“ClearFormatting”方法来删除所有边框。
foreach (Paragraph paragraph in doc.FirstSection.Body.Paragraphs)
{
    paragraph.ParagraphFormat.Borders.ClearFormatting();

    foreach (Border border in paragraph.ParagraphFormat.Borders)
    {
        Assert.AreEqual(Color.Empty.ToArgb(), border.Color.ToArgb());
        Assert.AreEqual(LineStyle.None, border.LineStyle);
        Assert.AreEqual(0.0d, border.LineWidth);
    }
}

doc.Save(ArtifactsDir + "BorderCollection.RemoveAllBorders.docx");
```

### 也可以看看

* class [BorderCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
