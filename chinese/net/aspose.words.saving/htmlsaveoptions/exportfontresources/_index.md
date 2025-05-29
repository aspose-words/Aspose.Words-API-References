---
title: HtmlSaveOptions.ExportFontResources
linktitle: ExportFontResources
articleTitle: ExportFontResources
second_title: Aspose.Words for .NET
description: 探索 HtmlSaveOptions ExportFontResources 属性，控制 HTML、MHTML 或 EPUB 格式的字体资源导出。最大限度地提升文档的视觉吸引力！
type: docs
weight: 140
url: /zh/net/aspose.words.saving/htmlsaveoptions/exportfontresources/
---
## HtmlSaveOptions.ExportFontResources property

指定是否应将字体资源导出为 HTML、MHTML 或 EPUB。 默认值为`错误的`.

```csharp
public bool ExportFontResources { get; set; }
```

## 评论

导出字体资源允许独立于给定用户环境中可用的字体实现一致的文档渲染。

如果`ExportFontResources`设置为`真的` ，主 HTML 文档将引用每个字体 via CSS 3**@font-face** at-rule 和字体将作为单独的文件输出。导出为 IDPF EPUB 或 MHTML 格式时，字体将与其他附属文件一起嵌入到相应的包中。

如果[`ExportFontsAsBase64`](../exportfontsasbase64/)设置为`真的` ，字体将不会保存到单独的文件中。 相反，它们将嵌入到**@font-face**Base64 编码中的 at-rules。

**重要的！**导出字体资源时，应考虑字体许可问题。希望通过可下载字体机制使用特定字体的作者必须始终仔细验证其预期用途是否在字体许可范围内。目前，许多商业字体不允许以任何形式在网络上下载其字体。涵盖某些字体的许可协议明确指出，通过**@font-face**CSS 样式表中的 rules 是不允许的。字体子集设置也可能违反许可条款。

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

* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
