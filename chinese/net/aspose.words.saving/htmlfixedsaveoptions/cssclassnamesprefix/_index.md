---
title: HtmlFixedSaveOptions.CssClassNamesPrefix
linktitle: CssClassNamesPrefix
articleTitle: CssClassNamesPrefix
second_title: 用于 .NET 的 Aspose.Words
description: HtmlFixedSaveOptions CssClassNamesPrefix 财产. 指定添加到 style.css 文件中所有类名的前缀 默认值为噢 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.saving/htmlfixedsaveoptions/cssclassnamesprefix/
---
## HtmlFixedSaveOptions.CssClassNamesPrefix property

指定添加到 style.css 文件中所有类名的前缀。 默认值为`“噢”`.

```csharp
public string CssClassNamesPrefix { get; set; }
```

## 例子

演示如何将 CSS 放入单独的文件中并为其所有 CSS 类名称添加前缀。

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
