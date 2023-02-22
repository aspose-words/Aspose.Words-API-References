---
title: FixedPageSaveOptions.PageSavingCallback
second_title: Aspose.Words for .NET API 参考
description: FixedPageSaveOptions 财产. 允许控制在将文档导出为固定页面格式时如何保存单独的页面
type: docs
weight: 60
url: /zh/net/aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/
---
## FixedPageSaveOptions.PageSavingCallback property

允许控制在将文档导出为固定页面格式时如何保存单独的页面。

```csharp
public IPageSavingCallback PageSavingCallback { get; set; }
```

### 例子

演示如何使用回调将文档逐页保存到 HTML。

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

    // 创建一个“HtmlFixedSaveOptions”对象，我们可以将它传递给文档的“Save”方法
    // 修改我们如何将文档转换为 HTML。
    HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();

    // 我们会将本文档中的每一页保存到本地文件系统中的单独 HTML 文件中。
    // 设置允许我们命名每个输出 HTML 文档的回调。
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

        // 下面是指定 Aspose.Words 将文档的每一页保存在哪里的两种方法。
        // 1 - 为输出页面文件设置文件名：
        args.PageFileName = outFileName;

        // 2 - 为输出页面文件创建自定义流：
        args.PageStream = new FileStream(outFileName, FileMode.Create);

        Assert.False(args.KeepPageStreamOpen);
    }
}
```

### 也可以看看

* interface [IPageSavingCallback](../../ipagesavingcallback/)
* class [FixedPageSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../fixedpagesaveoptions/)
* 部件 [Aspose.Words](../../../)


