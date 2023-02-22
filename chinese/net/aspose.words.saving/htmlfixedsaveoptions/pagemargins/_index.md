---
title: HtmlFixedSaveOptions.PageMargins
second_title: Aspose.Words for .NET API 参考
description: HtmlFixedSaveOptions 财产. 指定 HTML 文档中页面周围的边距 边距值以磅为单位应等于或大于 0 默认值为 10 磅
type: docs
weight: 120
url: /zh/net/aspose.words.saving/htmlfixedsaveoptions/pagemargins/
---
## HtmlFixedSaveOptions.PageMargins property

指定 HTML 文档中页面周围的边距。 边距值以磅为单位，应等于或大于 0。 默认值为 10 磅。

```csharp
public double PageMargins { get; set; }
```

### 评论

取决于价值[`PageHorizontalAlignment`](../pagehorizontalalignment/)财产：

* 如果值为Left.
* 如果值为Right.
* 如果值为Center.

### 例子

显示将文档保存为 HTML 时如何调整页边距。

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
* 命名空间 [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* 部件 [Aspose.Words](../../../)


