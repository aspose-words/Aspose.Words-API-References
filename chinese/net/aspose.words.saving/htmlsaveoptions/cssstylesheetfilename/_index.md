---
title: HtmlSaveOptions.CssStyleSheetFileName
linktitle: CssStyleSheetFileName
articleTitle: CssStyleSheetFileName
second_title: 用于 .NET 的 Aspose.Words
description: HtmlSaveOptions CssStyleSheetFileName 财产. 指定将文档 导出为 HTML 时写入的级联样式表 CSS 文件的路径和名称 默认为空字符串 在 C#.
type: docs
weight: 50
url: /zh/net/aspose.words.saving/htmlsaveoptions/cssstylesheetfilename/
---
## HtmlSaveOptions.CssStyleSheetFileName property

指定将文档 导出为 HTML 时写入的级联样式表 (CSS) 文件的路径和名称。 默认为空字符串。

```csharp
public string CssStyleSheetFileName { get; set; }
```

## 评论

仅当将文档保存为 HTML 格式 并且使用请求外部 CSS 样式表时，此属性才有效[`CssStyleSheetType`](../cssstylesheettype/)。

如果此属性为空，则 CSS 文件将保存到与 HTML 文档相同的文件夹中，并具有相同的名称，但扩展名为“.css”。

如果在此属性中仅指定路径但未指定文件名，则 CSS 文件将保存到指定的 文件夹中，并且与 HTML 文档同名，但扩展名为“.css”。

如果此属性指定的文件夹不存在，则会在保存 CSS file 之前自动创建该文件夹。

指定保存外部 CSS 文件的文件夹的另一种方法是使用[`ResourceFolder`](../resourcefolder/).

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

* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
