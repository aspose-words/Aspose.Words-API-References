---
title: HtmlSaveOptions
linktitle: HtmlSaveOptions
articleTitle: HtmlSaveOptions
second_title: Aspose.Words for .NET
description: 探索 HtmlSaveOptions 构造函数，轻松创建和保存 HTML 格式的文档，确保最佳格式和轻松共享。
type: docs
weight: 10
url: /zh/net/aspose.words.saving/htmlsaveoptions/htmlsaveoptions/
---
## HtmlSaveOptions() {#constructor}

初始化此类的新实例，可用于保存 document 在Html格式.

```csharp
public HtmlSaveOptions()
```

## 例子

展示如何在将文档保存为 .epub 时使用特定编码。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// 使用 SaveOptions 对象指定我们将保存的文档的编码。
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// 默认情况下，输出的 .epub 文档的所有内容都包含在一个 HTML 部分中。
// 拆分标准允许我们将文档分成几个 HTML 部分。
// 我们将设置标准将文档拆分为标题段落。
// 这对于无法读取大于特定大小的 HTML 文件的读者很有用。
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// 指定我们想要导出文档属性。
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### 也可以看看

* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)

---

## HtmlSaveOptions(*[SaveFormat](../../../aspose.words/saveformat/)*) {#constructor_1}

初始化此类的新实例，可用于保存 document 在Html，Mhtml，Epub , Azw3或者Mobi格式.

```csharp
public HtmlSaveOptions(SaveFormat saveFormat)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| saveFormat | SaveFormat | 可以Html，Mhtml，Epub , Azw3或者Mobi. |

## 例子

展示如何将文档保存为特定版本的 HTML。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    HtmlVersion = htmlVersion,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.HtmlVersions.html", options);

// 我们的 HTML 文档会有细微的差别，以兼容不同的 HTML 版本。
string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.HtmlVersions.html");

switch (htmlVersion)
{
    case HtmlVersion.Html5:
        Assert.True(outDocContents.Contains("<a id=\"_Toc76372689\"></a>"));
        Assert.True(outDocContents.Contains("<a id=\"_Toc76372689\"></a>"));
        Assert.True(outDocContents.Contains("<table style=\"padding:0pt; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
        break;
    case HtmlVersion.Xhtml:
        Assert.True(outDocContents.Contains("<a name=\"_Toc76372689\"></a>"));
        Assert.True(outDocContents.Contains("<ul type=\"disc\" style=\"margin:0pt; padding-left:0pt\">"));
        Assert.True(outDocContents.Contains("<table cellspacing=\"0\" cellpadding=\"0\" style=\"-aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\""));
        break;
}
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
