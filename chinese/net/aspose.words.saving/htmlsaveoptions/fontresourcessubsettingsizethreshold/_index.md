---
title: HtmlSaveOptions.FontResourcesSubsettingSizeThreshold
linktitle: FontResourcesSubsettingSizeThreshold
articleTitle: FontResourcesSubsettingSizeThreshold
second_title: Aspose.Words for .NET
description: 使用 FontResourcesSubsettingSizeThreshold 属性优化您的 HTML、MHTML 或 EPUB 文件，确保高效的字体资源管理。默认值为 0。
type: docs
weight: 290
url: /zh/net/aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold/
---
## HtmlSaveOptions.FontResourcesSubsettingSizeThreshold property

控制保存为 HTML、MHTML 或 EPUB 时需要子集化的字体资源。 默认值为`0`.

```csharp
public int FontResourcesSubsettingSizeThreshold { get; set; }
```

## 评论

[`ExportFontResources`](../exportfontresources/)允许将字体导出为子文件或 output 包的一部分。如果文档使用大量字体，尤其是包含大量字形，则输出大小可能会显著增大。字体子集功能通过过滤当前文档未使用的字形来减小导出字体资源的大小。

字体子集的工作原理如下：

* 默认情况下，所有导出的字体都是子集。
* 环境`FontResourcesSubsettingSizeThreshold`为正值 指示 Aspose.Words 对文件大小大于指定值的字体进行子集化。
* 将属性设置为MaxValue 抑制字体子集。

**重要的！**导出字体资源时，应考虑字体许可问题。希望通过可下载字体机制使用特定字体的作者必须始终仔细验证其预期用途是否在字体许可范围内。目前，许多商业字体不允许以任何形式在网络上下载其字体。涵盖某些字体的许可协议明确指出，通过**@font-face**CSS 样式表中的 rules 是不允许的。字体子集设置也可能违反许可条款。

## 例子

展示如何使用字体子集。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Times New Roman";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("Hello world!");

// 当我们将文档保存为 HTML 时，我们可以传递一个 SaveOptions 对象来配置字体子集。
// 假设我们将“ExportFontResources”标志设置为“true”，并在“FontsFolder”属性中命名一个文件夹。
// 在这种情况下，保存操作将创建该文件夹并在其中放置一个 .ttf 文件
// 我们的文档使用的每种字体的文件夹。
// 每个 .ttf 文件将包含该字体的整个字形集，
// 这可能会导致文档附带一个非常大的文件。
// 当我们对字体应用子集时，其导出的原始数据将仅包含文档的字形
// 使用而不是整个字形集。如果我们文档中的文本仅使用字体的一小部分
// 字形集，然后子集将显著减少我们输出文档的大小。
// 我们可以使用“FontResourcesSubsettingSizeThreshold”属性来定义.ttf 文件大小（以字节为单位）。
 // 如果导出的字体创建的文件比该字体更大，则保存操作将对该字体应用子集。
// 设置阈值 0 将对所有字体应用子集，
// 并将其设置为“int.MaxValue”可有效禁用子集。
string fontsFolder = ArtifactsDir + "HtmlSaveOptions.FontSubsetting.Fonts";

HtmlSaveOptions options = new HtmlSaveOptions
{
    ExportFontResources = true,
    FontsFolder = fontsFolder,
    FontResourcesSubsettingSizeThreshold = fontResourcesSubsettingSizeThreshold
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.FontSubsetting.html", options);

string[] fontFileNames = Directory.GetFiles(fontsFolder).Where(s => s.EndsWith(".ttf")).ToArray();

Assert.AreEqual(3, fontFileNames.Length);

foreach (string filename in fontFileNames)
{
    // 默认情况下，我们的三种字体的 .ttf 文件都将超过 700MB。
    // 子集将把它们全部减少到 30MB 以下。
    FileInfo fontFileInfo = new FileInfo(filename);

    Assert.True(fontFileInfo.Length > 700000 || fontFileInfo.Length < 30000);
    Assert.True(Math.Max(fontResourcesSubsettingSizeThreshold, 30000) > new FileInfo(filename).Length);
}
```

### 也可以看看

* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
