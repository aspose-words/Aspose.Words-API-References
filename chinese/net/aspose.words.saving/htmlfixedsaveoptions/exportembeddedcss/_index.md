---
title: HtmlFixedSaveOptions.ExportEmbeddedCss
linktitle: ExportEmbeddedCss
articleTitle: ExportEmbeddedCss
second_title: 用于 .NET 的 Aspose.Words
description: HtmlFixedSaveOptions ExportEmbeddedCss 财产. 指定 CSS层叠样式表是否应嵌入到 Html 文档中 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedcss/
---
## HtmlFixedSaveOptions.ExportEmbeddedCss property

指定 CSS（层叠样式表）是否应嵌入到 Html 文档中。

```csharp
public bool ExportEmbeddedCss { get; set; }
```

## 例子

演示将文档导出为 Html 时如何确定 CSS 样式表的存储位置。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// 当我们将文档导出为 html 时，Aspose.Words 还将创建一个 CSS 样式表来格式化文档。
// 将“ExportEmbeddedCss”标志设置为“true”，将 CSS 样式表保存到 .css 文件，
// 并使用 <link> 从 html 文档链接到该文件元素。
// 将标志设置为“false”将在 Html 文档中嵌入 CSS 样式表，
// 这只会创建一个文件而不是两个。
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedCss = exportEmbeddedCss
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss.html");

if (exportEmbeddedCss)
{
    Assert.True(Regex.Match(outDocContents, "<style type=\"text/css\">").Success);
    Assert.False(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"));
}
else
{
    Assert.True(Regex.Match(outDocContents,
        "<link rel=\"stylesheet\" type=\"text/css\" href=\"HtmlFixedSaveOptions[.]ExportEmbeddedCss/styles[.]css\" media=\"all\" />").Success);
    Assert.True(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"));
}
```

### 也可以看看

* class [HtmlFixedSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
