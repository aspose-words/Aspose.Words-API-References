---
title: MarkdownLoadOptions.ImportUnderlineFormatting
linktitle: ImportUnderlineFormatting
articleTitle: ImportUnderlineFormatting
second_title: Aspose.Words for .NET
description: 探索 MarkdownLoadOptions ImportUnderlineFormatting 属性。只需简单的布尔值设置即可控制下划线文本格式。提升您的 Markdown 体验！
type: docs
weight: 20
url: /zh/net/aspose.words.loading/markdownloadoptions/importunderlineformatting/
---
## MarkdownLoadOptions.ImportUnderlineFormatting property

获取或设置一个布尔值，指示是否将两个加号字符“++”的序列识别为下划线文本格式。 默认值为`错误的`.

```csharp
public bool ImportUnderlineFormatting { get; set; }
```

## 例子

展示如何将加号“++”识别为下划线文本格式。

```csharp
using (MemoryStream stream = new MemoryStream(Encoding.ASCII.GetBytes("++12 and B++")))
{
    MarkdownLoadOptions loadOptions = new MarkdownLoadOptions() { ImportUnderlineFormatting = true };
    Document doc = new Document(stream, loadOptions);

    Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
    Assert.AreEqual(Underline.Single, para.Runs[0].Font.Underline);

    loadOptions = new MarkdownLoadOptions() { ImportUnderlineFormatting = false };
    doc = new Document(stream, loadOptions);

    para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
    Assert.AreEqual(Underline.None, para.Runs[0].Font.Underline);
}
```

### 也可以看看

* class [MarkdownLoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
