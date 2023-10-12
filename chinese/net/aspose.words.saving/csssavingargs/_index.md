---
title: Class CssSavingArgs
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Saving.CssSavingArgs 班级. 提供数据CssSaving事件.
type: docs
weight: 4880
url: /zh/net/aspose.words.saving/csssavingargs/
---
## CssSavingArgs class

提供数据[`CssSaving`](../icsssavingcallback/csssaving/)事件.

要了解更多信息，请访问[保存文档](https://docs.aspose.com/words/net/save-a-document/)文档文章。

```csharp
public class CssSavingArgs
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [CssStream](../../aspose.words.saving/csssavingargs/cssstream/) { get; set; } | 允许指定 CSS 信息将保存到的流。 |
| [Document](../../aspose.words.saving/csssavingargs/document/) { get; } | 获取当前正在保存的文档对象。 |
| [IsExportNeeded](../../aspose.words.saving/csssavingargs/isexportneeded/) { get; set; } | 允许指定 CSS 是否导出到文件并嵌入到 HTML 文档。默认为`真的`. 当此属性为`错误的`，CSS信息不会保存到CSS文件中，也不会嵌入到HTML文档中。 |
| [KeepCssStreamOpen](../../aspose.words.saving/csssavingargs/keepcssstreamopen/) { get; set; } | 指定 Aspose.Words 在保存 CSS 信息后是否应保持流打开或关闭它。 |

### 评论

默认情况下，当 Aspose.Words 将文档保存为 HTML 时，它会保存 CSS 信息 inline （作为 **风格**每个元素上的属性）.

`CssSavingArgs`允许通过提供您自己的流对象将 CSS 信息保存到文件中。

要将 CSS 保存到流中，请使用[`CssStream`](./cssstream/)财产。

要禁止将 CSS 保存到文件中并嵌入到 HTML 文档中，请使用[`IsExportNeeded`](./isexportneeded/)财产。

### 例子

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

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)


