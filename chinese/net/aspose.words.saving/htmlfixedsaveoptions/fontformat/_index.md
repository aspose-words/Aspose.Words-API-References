---
title: HtmlFixedSaveOptions.FontFormat
linktitle: FontFormat
articleTitle: FontFormat
second_title: Aspose.Words for .NET
description: 探索 HtmlFixedSaveOptions FontFormat 属性，自定义字体导出。轻松设置并优化默认格式为 Woff，以获得更佳性能。
type: docs
weight: 90
url: /zh/net/aspose.words.saving/htmlfixedsaveoptions/fontformat/
---
## HtmlFixedSaveOptions.FontFormat property

获取或设置[`ExportFontFormat`](../../exportfontformat/)用于字体导出。 默认值为Woff.

```csharp
public ExportFontFormat FontFormat { get; set; }
```

## 例子

展示如何将文档保存为 HTML 时仅使用目标机器的字体。

```csharp
Document doc = new Document(MyDir + "Bullet points with alternative font.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedCss = true,
    UseTargetMachineFonts = useTargetMachineFonts,
    FontFormat = ExportFontFormat.Ttf,
    ExportEmbeddedFonts = false,
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.UsingMachineFonts.html");

if (useTargetMachineFonts)
    Assert.False(Regex.Match(outDocContents, "@font-face").Success);
else
    Assert.True(Regex.Match(outDocContents,
        "@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], " +
        "url[(]'HtmlFixedSaveOptions.UsingMachineFonts/font001.ttf'[)] format[(]'truetype'[)]; }").Success);
```

### 也可以看看

* enum [ExportFontFormat](../../exportfontformat/)
* class [HtmlFixedSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
