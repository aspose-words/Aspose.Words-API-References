---
title: HtmlFixedSaveOptions.ExportEmbeddedCss
linktitle: ExportEmbeddedCss
articleTitle: ExportEmbeddedCss
second_title: Aspose.Words for .NET
description: 了解 HtmlFixedSaveOptions 的 ExportEmbeddedCss 属性如何通过嵌入 CSS 实现无缝样式，从而增强您的 HTML 文档。立即优化您的网页！
type: docs
weight: 40
url: /zh/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedcss/
---
## HtmlFixedSaveOptions.ExportEmbeddedCss property

指定是否应将 CSS（层叠样式表）嵌入到 Html 文档中。

```csharp
public bool ExportEmbeddedCss { get; set; }
```

## 例子

展示如何确定将文档导出为 Html 时存储 CSS 样式表的位置。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// 当我们将文档导出为 html 时，Aspose.Words 还将创建一个 CSS 样式表来格式化文档。
// 将“ExportEmbeddedCss”标志设置为“true”，将 CSS 样式表保存到 .css 文件，
// 并使用 <link> 元素从 html 文档链接到该文件。
// 将标志设置为“false”将会在 HTML 文档中嵌入 CSS 样式表，
// 这将只创建一个文件而不是两个。
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
