---
title: PageSavingArgs Class
linktitle: PageSavingArgs
articleTitle: PageSavingArgs
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Saving.PageSavingArgs 类，它对于使用详细的 PageSaving 事件数据优化文档处理至关重要。增强您的工作流程！
type: docs
weight: 6160
url: /zh/net/aspose.words.saving/pagesavingargs/
---
## PageSavingArgs class

为[`PageSaving`](../ipagesavingcallback/pagesaving/)事件.

要了解更多信息，请访问[使用文档进行编程](https://docs.aspose.com/words/net/programming-with-documents/)文档文章。

```csharp
public class PageSavingArgs
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [PageSavingArgs](pagesavingargs/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [KeepPageStreamOpen](../../aspose.words.saving/pagesavingargs/keeppagestreamopen/) { get; set; } | 指定 Aspose.Words 是否应保持流打开或在保存文档页面后关闭它。 |
| [PageFileName](../../aspose.words.saving/pagesavingargs/pagefilename/) { get; set; } | 获取或设置将保存文档页面的文件名。 |
| [PageIndex](../../aspose.words.saving/pagesavingargs/pageindex/) { get; } | 当前页面索引。 |
| [PageStream](../../aspose.words.saving/pagesavingargs/pagestream/) { get; set; } | 允许指定将文档页面保存到的流。 |

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

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
