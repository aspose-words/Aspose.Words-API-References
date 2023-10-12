---
title: HtmlSaveOptions.ExportFontResources
second_title: Aspose.Words for .NET API 参考
description: HtmlSaveOptions 财产. 指定是否应将字体资源导出为 HTMLMHTML 或 EPUB 默认为错误的.
type: docs
weight: 140
url: /zh/net/aspose.words.saving/htmlsaveoptions/exportfontresources/
---
## HtmlSaveOptions.ExportFontResources property

指定是否应将字体资源导出为 HTML、MHTML 或 EPUB。 默认为`错误的`.

```csharp
public bool ExportFontResources { get; set; }
```

### 评论

导出字体资源允许在给定用户环境中独立于可用 字体实现一致的文档渲染。

如果`ExportFontResources`被设定为`真的` , 主 HTML 文档将通过 CSS 3 引用每种字体 **@字体脸**at-rule 和字体将作为单独的文件输出。导出为 IDPF EPUB 或 MHTML 格式时，字体将与其他附属文件一起嵌入到相应的包中。

如果[`ExportFontsAsBase64`](../exportfontsasbase64/)被设定为`真的`，字体不会保存到单独的文件中。 相反，它们将嵌入到 **@字体脸**Base64 编码中的 at 规则。

**重要的！**导出字体资源时，应考虑字体许可问题。想要通过 downloadable 字体机制使用特定字体的作者必须始终仔细验证其预期用途是否在字体许可证的范围内。目前，许多商业字体不允许 以任何形式通过网络下载其字体。涵盖某些字体的许可协议特别指出，通过 **@字体脸**CSS 样式表中不允许使用rules 。字体子集设置也可能违反许可条款。

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

* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../htmlsaveoptions/)
* 部件 [Aspose.Words](../../../)


