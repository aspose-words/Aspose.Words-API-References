---
title: CssSavingArgs.CssStream
linktitle: CssStream
articleTitle: CssStream
second_title: 用于 .NET 的 Aspose.Words
description: CssSavingArgs CssStream 财产. 允许指定 CSS 信息将保存到的流 在 C#.
type: docs
weight: 10
url: /zh/net/aspose.words.saving/csssavingargs/cssstream/
---
## CssSavingArgs.CssStream property

允许指定 CSS 信息将保存到的流。

```csharp
public Stream CssStream { get; set; }
```

## 评论

此属性允许您将 CSS 信息保存到流中。

默认值为`无效的` 。此属性不会禁止将 CSS 信息保存到文件或 嵌入到 HTML 文档。要禁止导出 CSS，请使用[`IsExportNeeded`](../isexportneeded/)财产。

使用[`ICssSavingCallback`](../../icsssavingcallback/)你不能用 另一个替代CSS。它仅用于将 CSS 保存到流中。

## 例子

演示如何使用 HTML 转换创建的 CSS 样式表。

```csharp
public void ExternalCssFilenames()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // 创建一个“HtmlFixedSaveOptions”对象，我们可以将其传递给文档的“Save”方法
    // 修改我们将文档转换为 HTML 的方式。
    HtmlSaveOptions options = new HtmlSaveOptions();

    // 将“CssStylesheetType”属性设置为“CssStyleSheetType.External”即可
    // 保存的 HTML 文档附带外部 CSS 样式表文件。
    options.CssStyleSheetType = CssStyleSheetType.External;

    // 以下是指定输出 CSS 样式表的目录和文件名的两种方法。
    // 1 - 使用“CssStyleSheetFileName”属性为样式表分配文件名：
    options.CssStyleSheetFileName = ArtifactsDir + "SavingCallback.ExternalCssFilenames.css";

    // 2 - 使用自定义回调来命名我们的样式表：
    options.CssSavingCallback =
        new CustomCssSavingCallback(ArtifactsDir + "SavingCallback.ExternalCssFilenames.css", true, false);

    doc.Save(ArtifactsDir + "SavingCallback.ExternalCssFilenames.html", options);
}

/// <summary>
/// 设置自定义文件名以及外部 CSS 样式表的其他参数。
/// </summary>
private class CustomCssSavingCallback : ICssSavingCallback
{
    public CustomCssSavingCallback(string cssDocFilename, bool isExportNeeded, bool keepCssStreamOpen)
    {
        mCssTextFileName = cssDocFilename;
        mIsExportNeeded = isExportNeeded;
        mKeepCssStreamOpen = keepCssStreamOpen;
    }

    public void CssSaving(CssSavingArgs args)
    {
        // 我们可以通过“Document”属性访问整个源文档。
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        args.CssStream = new FileStream(mCssTextFileName, FileMode.Create);
        args.IsExportNeeded = mIsExportNeeded;
        args.KeepCssStreamOpen = mKeepCssStreamOpen;

        Assert.True(args.CssStream.CanWrite);
    }

    private readonly string mCssTextFileName;
    private readonly bool mIsExportNeeded;
    private readonly bool mKeepCssStreamOpen;
}
```

### 也可以看看

* class [CssSavingArgs](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
