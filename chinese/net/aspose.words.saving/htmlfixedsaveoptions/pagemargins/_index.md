---
title: HtmlFixedSaveOptions.PageMargins
linktitle: PageMargins
articleTitle: PageMargins
second_title: 用于 .NET 的 Aspose.Words
description: HtmlFixedSaveOptions PageMargins 财产. 指定 HTML 文档中页面周围的边距 边距值以磅为单位测量应等于或大于 0 默认值为 10 磅 在 C#.
type: docs
weight: 120
url: /zh/net/aspose.words.saving/htmlfixedsaveoptions/pagemargins/
---
## HtmlFixedSaveOptions.PageMargins property

指定 HTML 文档中页面周围的边距。 边距值以磅为单位测量，应等于或大于 0。 默认值为 10 磅。

```csharp
public double PageMargins { get; set; }
```

## 评论

取决于值[`PageHorizontalAlignment`](../pagehorizontalalignment/)财产：

* 定义上页边距、下页边距和左页边距（如果该值为Left.
* 定义上页边距、下页边距和右页边距（如果该值为Right.
* 定义顶部和底部页边距（如果值为）Center.

## 例子

演示将文档保存为 HTML 时如何调整页边距。

```csharp
Document doc = new Document(MyDir + "Document.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions
{
    PageMargins = 15
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.PageMargins.html", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.PageMargins/styles.css");

Assert.True(Regex.Match(outDocContents,
    "[.]awpage { position:relative; border:solid 1pt black; margin:15pt auto 15pt auto; overflow:hidden; }").Success);
```

### 也可以看看

* class [HtmlFixedSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
