---
title: Interface IFontSavingCallback
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Saving.IFontSavingCallback 界面. 如果您想接收通知并控制如何接收通知请实现此接口 Aspose.Words 在将文档导出为 HTML 格式时保存字体
type: docs
weight: 4900
url: /zh/net/aspose.words.saving/ifontsavingcallback/
---
## IFontSavingCallback interface

如果您想接收通知并控制如何接收通知，请实现此接口 Aspose.Words 在将文档导出为 HTML 格式时保存字体。

```csharp
public interface IFontSavingCallback
```

## 方法

| 姓名 | 描述 |
| --- | --- |
| [FontSaving](../../aspose.words.saving/ifontsavingcallback/fontsaving/)(FontSavingArgs) | 在 Aspose.Words 即将保存字体资源时调用。 |

### 例子

展示如何定义自定义逻辑以在保存为 HTML 时导出字体。

```csharp
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // 配置 SaveOptions 对象以将字体导出到单独的文件。
    // 设置一个以自定义方式处理字体保存的回调。
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

/// <summary>
/// 打印有关导出字体的信息并将它们保存在与其输出 .html 相同的本地系统文件夹中。
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

        // 有两种保存导出字体的方法。
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


