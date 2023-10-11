---
title: HtmlSaveOptions.ResolveFontNames
second_title: Aspose.Words for .NET API 参考
description: HtmlSaveOptions 财产. 指定是否根据 解析和替换文档中使用的字体系列名称FontSettings当写入基于 HTML 的格式时
type: docs
weight: 410
url: /zh/net/aspose.words.saving/htmlsaveoptions/resolvefontnames/
---
## HtmlSaveOptions.ResolveFontNames property

指定是否根据 解析和替换文档中使用的字体系列名称[`FontSettings`](../../../aspose.words/document/fontsettings/)当写入基于 HTML 的格式时。

```csharp
public bool ResolveFontNames { get; set; }
```

### 评论

默认情况下，该选项设置为`错误的`字体系列名称将按照源文档中指定的 写入 HTML。那是，[`FontSettings`](../../../aspose.words/document/fontsettings/)被忽略，并且不执行字体系列名称的解析或替换 。

如果该选项设置为`真的`、Aspose.Words 使用[`FontSettings`](../../../aspose.words/document/fontsettings/)将源文档中指定的每个字体系列名称解析为可用字体系列的名称，并根据需要执行字体替换。

### 例子

演示如何在将所有字体名称写入 HTML 之前解析它们。

```csharp
Document doc = new Document(MyDir + "Missing font.docx");

// 该文档包含命名我们没有的字体的文本。
Assert.NotNull(doc.FontInfos["28 Days Later"]);

// 如果我们无法获得这种字体，并且我们希望能够显示所有文本
// 在这个文档的输出 HTML 中，我们可以用另一种字体替换它。
FontSettings fontSettings = new FontSettings
{
    SubstitutionSettings =
    {
        DefaultFontSubstitution =
        {
            DefaultFontName = "Arial",
            Enabled = true
        }
    }
};

doc.FontSettings = fontSettings;

HtmlSaveOptions saveOptions = new HtmlSaveOptions(SaveFormat.Html)
{
    // 默认情况下，此选项设置为“False”，Aspose.Words 按照源文档中指定的方式写入字体名称
    ResolveFontNames = resolveFontNames
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ResolveFontNames.html", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ResolveFontNames.html");

Assert.True(resolveFontNames
    ? Regex.Match(outDocContents, "<span style=\"font-family:Arial\">").Success
    : Regex.Match(outDocContents, "<span style=\"font-family:\'28 Days Later\'\">").Success);
```

### 也可以看看

* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../htmlsaveoptions/)
* 部件 [Aspose.Words](../../../)


