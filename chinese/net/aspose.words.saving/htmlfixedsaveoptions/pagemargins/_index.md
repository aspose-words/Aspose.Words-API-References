---
title: HtmlFixedSaveOptions.PageMargins
linktitle: PageMargins
articleTitle: PageMargins
second_title: Aspose.Words for .NET
description: 探索 HtmlFixedSaveOptions PageMargins 属性，自定义 HTML 文档的边距。以磅为单位设置值，实现精确的布局控制。
type: docs
weight: 130
url: /zh/net/aspose.words.saving/htmlfixedsaveoptions/pagemargins/
---
## HtmlFixedSaveOptions.PageMargins property

指定 HTML 文档中页面周围的边距。 边距值以点为单位，应等于或大于 0。 默认值为 10 点。

```csharp
public double PageMargins { get; set; }
```

## 评论

取决于[`PageHorizontalAlignment`](../pagehorizontalalignment/)财产：

* 如果值为，则定义顶部、底部和左边距Left.
* 如果值为，则定义顶部、底部和右侧页边距Right.
* 定义顶部和底部页边距，如果值为Center.

## 例子

展示如何在将文档保存为 HTML 时调整页边距。

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
