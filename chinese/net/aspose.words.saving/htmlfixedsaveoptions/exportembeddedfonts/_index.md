---
title: HtmlFixedSaveOptions.ExportEmbeddedFonts
linktitle: ExportEmbeddedFonts
articleTitle: ExportEmbeddedFonts
second_title: 用于 .NET 的 Aspose.Words
description: HtmlFixedSaveOptions ExportEmbeddedFonts 财产. 指定字体是否应以 Base64 格式嵌入到 Html 文档中 请注意设置此标志会显着增加输出 Html 文件的大小 在 C#.
type: docs
weight: 50
url: /zh/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedfonts/
---
## HtmlFixedSaveOptions.ExportEmbeddedFonts property

指定字体是否应以 Base64 格式嵌入到 Html 文档中。 请注意，设置此标志会显着增加输出 Html 文件的大小。

```csharp
public bool ExportEmbeddedFonts { get; set; }
```

## 例子

演示将文档导出为 Html 时如何确定嵌入字体的存储位置。

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

// 当我们将嵌入字体的文档导出为 .html 时，
// Aspose.Words 可以将字体放置在两个可能的位置。
// 将“ExportEmbeddedFonts”标志设置为“true”将存储 CSS 样式表中嵌入字体的原始数据，
// 在“@font-face”规则的“url”属性中。这可能会创建一个巨大的 CSS 样式表文件
// 并减少此 HTML 转换将创建的外部文件的数量。
// 将此标志设置为“false”将为每种字体创建一个文件。
// CSS 样式表将使用“@font-face”规则的“url”属性链接到每个字体文件。
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedFonts = exportEmbeddedFonts
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedFonts.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedFonts/styles.css");

if (exportEmbeddedFonts)
{
    Assert.True(Regex.Match(outDocContents,
        "@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], url[(].+[)] format[(]'woff'[)]; }").Success);
    Assert.AreEqual(0, Directory.GetFiles(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedFonts").Count(f => f.EndsWith(".woff")));
}
else
{
    Assert.True(Regex.Match(outDocContents,
        "@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], url[(]'font001[.]woff'[)] format[(]'woff'[)]; }").Success);
    Assert.AreEqual(2, Directory.GetFiles(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedFonts").Count(f => f.EndsWith(".woff")));
}
```

### 也可以看看

* class [HtmlFixedSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
