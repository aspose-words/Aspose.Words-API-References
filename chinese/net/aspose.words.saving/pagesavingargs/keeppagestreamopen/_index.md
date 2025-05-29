---
title: PageSavingArgs.KeepPageStreamOpen
linktitle: KeepPageStreamOpen
articleTitle: KeepPageStreamOpen
second_title: Aspose.Words for .NET
description: 了解 PageSavingArgs 中的 KeepPageStreamOpen 属性如何通过控制流行为来实现最佳性能，从而增强 Aspose.Words 的文档管理。
type: docs
weight: 20
url: /zh/net/aspose.words.saving/pagesavingargs/keeppagestreamopen/
---
## PageSavingArgs.KeepPageStreamOpen property

指定 Aspose.Words 是否应保持流打开或在保存文档页面后关闭它。

```csharp
public bool KeepPageStreamOpen { get; set; }
```

## 评论

默认为`错误的`并且 Aspose.Words 将关闭您提供的流 [`PageStream`](../pagestream/)属性后将文档页面写入其中。 指定`真的`保持溪流畅通。

## 例子

展示如何使用回调将文档逐页保存为 HTML。

```csharp
public void PageFileNames()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Page 1.");
    builder.InsertBreak(BreakType.PageBreak);
    builder.Writeln("Page 2.");
    builder.InsertImage(ImageDir + "Logo.jpg");
    builder.InsertBreak(BreakType.PageBreak);
    builder.Writeln("Page 3.");

    // 创建一个“HtmlFixedSaveOptions”对象，我们可以将其传递给文档的“Save”方法
    // 修改我们将文档转换为 HTML 的方式。
    HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();

    // 我们将把该文档中的每个页面保存到本地文件系统中单独的 HTML 文件中。
    // 设置一个回调，允许我们命名每个输出 HTML 文档。
    htmlFixedSaveOptions.PageSavingCallback = new CustomFileNamePageSavingCallback();

    doc.Save(ArtifactsDir + "SavingCallback.PageFileNames.html", htmlFixedSaveOptions);

    string[] filePaths = Directory.GetFiles(ArtifactsDir).Where(
        s => s.StartsWith(ArtifactsDir + "SavingCallback.PageFileNames.Page_")).OrderBy(s => s).ToArray();

    Assert.AreEqual(3, filePaths.Length);
}

/// <summary>
/// 将所有页面保存到指定的文件和目录中。
/// </summary>
private class CustomFileNamePageSavingCallback : IPageSavingCallback
{
    public void PageSaving(PageSavingArgs args)
    {
        string outFileName = $"{ArtifactsDir}SavingCallback.PageFileNames.Page_{args.PageIndex}.html";

        // 以下是两种指定 Aspose.Words 保存文档每一页的位置的方法。
        // 1 - 为输出页面文件设置文件名：
        args.PageFileName = outFileName;

        // 2 - 为输出页面文件创建自定义流：
        args.PageStream = new FileStream(outFileName, FileMode.Create);

        Assert.False(args.KeepPageStreamOpen);
    }
}
```

### 也可以看看

* class [PageSavingArgs](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
