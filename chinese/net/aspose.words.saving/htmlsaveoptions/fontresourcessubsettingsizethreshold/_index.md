---
title: HtmlSaveOptions.FontResourcesSubsettingSizeThreshold
second_title: Aspose.Words for .NET API 参考
description: HtmlSaveOptions 财产. 控制保存为 HTMLMHTML 或 EPUB 时需要子集的字体资源 默认为0.
type: docs
weight: 300
url: /zh/net/aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold/
---
## HtmlSaveOptions.FontResourcesSubsettingSizeThreshold property

控制保存为 HTML、MHTML 或 EPUB 时需要子集的字体资源。 默认为`0`.

```csharp
public int FontResourcesSubsettingSizeThreshold { get; set; }
```

### 评论

[`ExportFontResources`](../exportfontresources/)允许将字体导出为辅助文件或 output 包的一部分。如果文档使用多种字体，尤其是使用大量字形，则输出大小会显着增长 。字体子集通过过滤掉当前文档未使用的 字形来减小导出字体资源的大小。

字体子集的工作方式如下：

* 默认情况下，所有导出的字体都是子集。
* 环境`FontResourcesSubsettingSizeThreshold`为正值 指示 Aspose.Words 对文件大小大于指定值的字体进行子集化。
* 将属性设置为MaxValue 抑制字体子集。

**重要的！**导出字体资源时，应考虑字体许可问题。希望通过可下载 字体机制使用特定字体的作者必须始终仔细验证其预期用途是否在字体许可范围内。许多商业字体目前不 允许以任何形式从网络下载他们的字体。涵盖某些字体的许可协议特别指出，使用 **@字体脸**不允许在 CSS 样式表中使用 rules 。字体子集也可能违反许可条款。

### 例子

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

// 当我们将文档保存为 HTML 时，我们可以传递一个 SaveOptions 对象配置字体子集。
// 假设我们将“ExportFontResources”标志设置为“true”，并在“FontsFolder”属性中命名一个文件夹。
// 在这种情况下，保存操作将创建该文件夹并在其中放置一个 .ttf 文件
// 我们文档使用的每种字体的文件夹。
// 每个 .ttf 文件将包含该字体的整个字形集，
// 这可能会导致文档附带一个非常大的文件。
// 当我们对字体应用子集时，其导出的原始数据将只包含文档所在的字形
// 使用而不是整个字形集。如果我们文档中的文本只使用了字体的一小部分
// 字形集，然后子集将显着减小我们输出文档的大小。
// 我们可以使用“FontResourcesSubsettingSizeThreshold”属性来定义一个 .ttf 文件的大小，以字节为单位。
 // 如果导出的字体创建的文件大小大于该文件，则保存操作将对该字体应用子集。
// 将阈值设置为 0 将子集应用于所有字体，
// 并将其设置为“int.MaxValue”有效地禁用子集。
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
    // 默认情况下，我们三种字体的 .ttf 文件都将超过 700MB。
    // 子集会将它们全部减少到 30MB 以下。
    FileInfo fontFileInfo = new FileInfo(filename);

    Assert.True(fontFileInfo.Length > 700000 || fontFileInfo.Length < 30000);
    Assert.True(Math.Max(fontResourcesSubsettingSizeThreshold, 30000) > new FileInfo(filename).Length);
}
```

### 也可以看看

* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../htmlsaveoptions/)
* 部件 [Aspose.Words](../../../)


