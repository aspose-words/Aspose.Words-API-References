---
title: HtmlFixedSaveOptions.SaveFontFaceCssSeparately
linktitle: SaveFontFaceCssSeparately
articleTitle: SaveFontFaceCssSeparately
second_title: Aspose.Words for .NET
description: 了解 SaveFontFaceCssSeparately 属性如何通过将字体规则保存在单独的文件中以实现更清晰的导出来优化文档的 CSS 管理。
type: docs
weight: 180
url: /zh/net/aspose.words.saving/htmlfixedsaveoptions/savefontfacecssseparately/
---
## HtmlFixedSaveOptions.SaveFontFaceCssSeparately property

标志指示当使用外部样式表保存文档时（即当[`ExportEmbeddedCss`](../exportembeddedcss/) 是`错误的`). 默认值为`错误的`，所有 CSS 规则都写入单个文件“styles.css”中。

```csharp
public bool SaveFontFaceCssSeparately { get; set; }
```

## 评论

将此属性设置为`真的`恢复旧行为（单独的文件）以兼容旧代码。

## 例子

展示如何将 CSS 放入单独的文件中并为其所有 CSS 类名添加前缀。

```csharp
Document doc = new Document(MyDir + "Bookmarks.docx");

HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    CssClassNamesPrefix = "myprefix",
    SaveFontFaceCssSeparately = true
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.AddCssClassNamesPrefix.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.AddCssClassNamesPrefix.html");

Assert.True(Regex.Match(outDocContents,
    "<div class=\"myprefixdiv myprefixpage\" style=\"width:595[.]3pt; height:841[.]9pt;\">" +
    "<div class=\"myprefixdiv\" style=\"left:85[.]05pt; top:36pt; clip:rect[(]0pt,510[.]25pt,74[.]95pt,-85.05pt[)];\">" +
    "<span class=\"myprefixspan myprefixtext001\" style=\"font-size:11pt; left:294[.]73pt; top:0[.]36pt; line-height:12[.]29pt;\">").Success);

outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.AddCssClassNamesPrefix/styles.css");

Assert.True(Regex.Match(outDocContents,
    ".myprefixdiv { position:absolute; } " +
    ".myprefixspan { position:absolute; white-space:pre; color:#000000; font-size:12pt; }").Success);
```

### 也可以看看

* class [HtmlFixedSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
