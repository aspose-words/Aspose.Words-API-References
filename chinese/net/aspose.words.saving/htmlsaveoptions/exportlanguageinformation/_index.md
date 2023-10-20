---
title: HtmlSaveOptions.ExportLanguageInformation
linktitle: ExportLanguageInformation
articleTitle: ExportLanguageInformation
second_title: 用于 .NET 的 Aspose.Words
description: HtmlSaveOptions ExportLanguageInformation 财产. 指定是否将语言信息导出为 HTMLMHTML 或 EPUB 默认为错误的 在 C#.
type: docs
weight: 180
url: /zh/net/aspose.words.saving/htmlsaveoptions/exportlanguageinformation/
---
## HtmlSaveOptions.ExportLanguageInformation property

指定是否将语言信息导出为 HTML、MHTML 或 EPUB。 默认为`错误的`.

```csharp
public bool ExportLanguageInformation { get; set; }
```

## 评论

当该属性设置为`真的`Aspose.Words 输出**郎**document 元素上指定语言的 HTML 属性。这可能需要保留语言相关的语义。

## 例子

演示如何在保存到 .html 时保留语言信息。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 使用构建器写入文本，同时在不同区域设置中格式化文本。
builder.Font.LocaleId = new CultureInfo("en-US").LCID;
builder.Writeln("Hello world!");

builder.Font.LocaleId = new CultureInfo("en-GB").LCID;
builder.Writeln("Hello again!");

builder.Font.LocaleId = new CultureInfo("ru-RU").LCID;
builder.Write("Привет, мир!");

// 将文档保存为 HTML 时，我们可以传递一个 SaveOptions 对象
// 保留或丢弃每个格式化文本的区域设置。
// 如果我们将“ExportLanguageInformation”标志设置为“true”，
// 输出 HTML 文档将包含 <span> 的“lang”属性中的语言环境标签。
// 如果我们将“ExportLanguageInformation”标志设置为“false”，
// 输出 HTML 文档中的文本将不包含任何区域设置信息。
HtmlSaveOptions options = new HtmlSaveOptions
{
    ExportLanguageInformation = exportLanguageInformation,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportLanguageInformation.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportLanguageInformation.html");

if (exportLanguageInformation)
{
    Assert.True(outDocContents.Contains("<span>Hello world!</span>"));
    Assert.True(outDocContents.Contains("<span lang=\"en-GB\">Hello again!</span>"));
    Assert.True(outDocContents.Contains("<span lang=\"ru-RU\">Привет, мир!</span>"));
}
else
{
    Assert.True(outDocContents.Contains("<span>Hello world!</span>"));
    Assert.True(outDocContents.Contains("<span>Hello again!</span>"));
    Assert.True(outDocContents.Contains("<span>Привет, мир!</span>"));
}
```

### 也可以看看

* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
