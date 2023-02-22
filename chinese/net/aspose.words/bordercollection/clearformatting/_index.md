---
title: BorderCollection.ClearFormatting
second_title: Aspose.Words for .NET API 参考
description: BorderCollection 方法. 删除对象的所有边框
type: docs
weight: 140
url: /zh/net/aspose.words/bordercollection/clearformatting/
---
## BorderCollection.ClearFormatting method

删除对象的所有边框。

```csharp
public void ClearFormatting()
```

### 例子

演示如何从文档中的所有段落中删除所有边框。

```csharp
Document doc = new Document(MyDir + "Borders.docx");

// 此文档的第一段具有这些设置的可见边框。
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
* 命名空间 [Aspose.Words](../../bordercollection/)
* 部件 [Aspose.Words](../../../)


