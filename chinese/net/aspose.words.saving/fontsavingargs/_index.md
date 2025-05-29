---
title: FontSavingArgs Class
linktitle: FontSavingArgs
articleTitle: FontSavingArgs
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Saving.FontSavingArgs 类——使用详细的 FontSaving 事件数据增强文档处理，实现卓越的定制和控制。
type: docs
weight: 5780
url: /zh/net/aspose.words.saving/fontsavingargs/
---
## FontSavingArgs class

为[`FontSaving`](../ifontsavingcallback/fontsaving/)事件.

要了解更多信息，请访问[保存文档](https://docs.aspose.com/words/net/save-a-document/)文档文章。

```csharp
public class FontSavingArgs
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Bold](../../aspose.words.saving/fontsavingargs/bold/) { get; } | 表示当前字体是否为粗体。 |
| [Document](../../aspose.words.saving/fontsavingargs/document/) { get; } | 获取正在保存的文档对象。 |
| [FontFamilyName](../../aspose.words.saving/fontsavingargs/fontfamilyname/) { get; } | 表示当前字体系列名称。 |
| [FontFileName](../../aspose.words.saving/fontsavingargs/fontfilename/) { get; set; } | 获取或设置字体将保存到的文件名（不带路径）。 |
| [FontStream](../../aspose.words.saving/fontsavingargs/fontstream/) { get; set; } | 允许指定字体保存到的流。 |
| [IsExportNeeded](../../aspose.words.saving/fontsavingargs/isexportneeded/) { get; set; } | 允许指定是否将当前字体导出为字体资源。默认为`真的`. |
| [IsSubsettingNeeded](../../aspose.words.saving/fontsavingargs/issubsettingneeded/) { get; set; } | 允许指定在导出为字体资源之前是否对当前字体进行子集化。 |
| [Italic](../../aspose.words.saving/fontsavingargs/italic/) { get; } | 表示当前字体是否为斜体。 |
| [KeepFontStreamOpen](../../aspose.words.saving/fontsavingargs/keepfontstreamopen/) { get; set; } | 指定 Aspose.Words 是否应保持流打开或保存字体后关闭它。 |
| [OriginalFileName](../../aspose.words.saving/fontsavingargs/originalfilename/) { get; } | 获取带有扩展名的原始字体文件名。 |
| [OriginalFileSize](../../aspose.words.saving/fontsavingargs/originalfilesize/) { get; } | 获取原始字体文件大小。 |

## 评论

当 Aspose.Words 将文档保存为 HTML 或相关格式时，[`ExportFontResources`](../htmlsaveoptions/exportfontresources/) 设置为`真的`，它将每个字体主题保存到单独的文件中以供导出。

`FontSavingArgs`控制是否导出特定字体资源以及如何导出。

`FontSavingArgs`还允许重新定义如何生成字体文件名，或者通过提供您自己的流对象来完全避免将字体保存到文件中。

要决定是否保存特定字体资源，请使用[`IsExportNeeded`](./isexportneeded/)财产。

要将字体保存到流而不是文件中，请使用[`FontStream`](./fontstream/)财产。

## 例子

展示如何在保存为 HTML 时定义导出字体的自定义逻辑。

```csharp
public void SaveExportedFonts()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // 配置一个 SaveOptions 对象以将字体导出到单独的文件。
    // 设置一个回调，以自定义方式处理字体保存。
    HtmlSaveOptions options = new HtmlSaveOptions
    {
        ExportFontResources = true,
        FontSavingCallback = new HandleFontSaving()
    };

    // 回调将导出 .ttf 文件并将其与输出文档一起保存。
    doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveExportedFonts.html", options);

    foreach (string fontFilename in Array.FindAll(Directory.GetFiles(ArtifactsDir), s => s.EndsWith(".ttf")))
    {
        Console.WriteLine(fontFilename);
    }

}

/// <summary>
/// 打印有关导出字体的信息并将其保存在与其输出 .html 相同的本地系统文件夹中。
/// </summary>
public class HandleFontSaving : IFontSavingCallback
{
    void IFontSavingCallback.FontSaving(FontSavingArgs args)
    {
        Console.Write($"Font:\t{args.FontFamilyName}");
        if (args.Bold) Console.Write(", bold");
        if (args.Italic) Console.Write(", italic");
        Console.WriteLine($"\nSource:\t{args.OriginalFileName}, {args.OriginalFileSize} bytes\n");

        // 我们也可以从这里访问源文档。
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        Assert.True(args.IsExportNeeded);
        Assert.True(args.IsSubsettingNeeded);

        // 有两种方法可以保存导出的字体。
        // 1 - 将其保存到本地文件系统位置：
        args.FontFileName = args.OriginalFileName.Split(Path.DirectorySeparatorChar).Last();

        // 2 - 将其保存到流中：
        args.FontStream =
            new FileStream(ArtifactsDir + args.OriginalFileName.Split(Path.DirectorySeparatorChar).Last(), FileMode.Create);
        Assert.False(args.KeepFontStreamOpen);
    }
}
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
