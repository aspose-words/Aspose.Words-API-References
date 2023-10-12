---
title: FontSavingArgs.FontFileName
second_title: Aspose.Words for .NET API 参考
description: FontSavingArgs 财产. 获取或设置保存字体的文件名不带路径
type: docs
weight: 40
url: /zh/net/aspose.words.saving/fontsavingargs/fontfilename/
---
## FontSavingArgs.FontFileName property

获取或设置保存字体的文件名（不带路径）。

```csharp
public string FontFileName { get; set; }
```

### 评论

此属性允许您重新定义导出到 HTML 期间如何生成字体文件名 。

当事件被触发时，该属性包含由 Aspose.Words 生成的文件名 。您可以更改此属性的值以将字体保存到 不同的文件中。请注意，文件名必须是唯一的。

当 导出为 HTML 格式时，Aspose.Words 会自动为每个嵌入字体生成唯一的文件名。字体文件名的生成方式 取决于您将文档保存到文件还是流中。

将文档保存到文件时，生成的字体文件名类似于 &lt;文档基本文件名&gt;.&lt;原始文件名&gt;&lt;可选后缀&gt;.&lt;扩展名&gt;。

将文档保存到流时，生成的字体文件名类似于 Aspose.Words.&lt;文档guid&gt;.&lt;原始文件名&gt;&lt;可选后缀&gt;.&lt;扩展名&gt;。

`FontFileName`必须仅包含文件名而不包含路径。 Aspose.Words 使用文档文件名确定保存路径， [`FontsFolder`](../../htmlsaveoptions/fontsfolder/)和 [`FontsFolderAlias`](../../htmlsaveoptions/fontsfolderalias/)特性。

### 例子

演示如何定义保存为 HTML 时导出字体的自定义逻辑。

```csharp
public void SaveExportedFonts()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // 配置 SaveOptions 对象以将字体导出到单独的文件。
    // 设置将以自定义方式处理字体保存的回调。
    HtmlSaveOptions options = new HtmlSaveOptions
    {
        ExportFontResources = true,
        FontSavingCallback = new HandleFontSaving()
    };

    // 回调将导出 .ttf 文件并将它们与输出文档一起保存。
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

        // 有两种方法保存导出的字体。
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

* class [FontSavingArgs](../)
* 命名空间 [Aspose.Words.Saving](../../fontsavingargs/)
* 部件 [Aspose.Words](../../../)


