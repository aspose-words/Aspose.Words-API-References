---
title: ResourceSavingArgs.ResourceFileName
linktitle: ResourceFileName
articleTitle: ResourceFileName
second_title: Aspose.Words for .NET
description: 使用 ResourceSavingArgs 高效管理您的资源。轻松设置或检索用于保存资源的文件名，无需费心设置路径。
type: docs
weight: 30
url: /zh/net/aspose.words.saving/resourcesavingargs/resourcefilename/
---
## ResourceSavingArgs.ResourceFileName property

获取或设置资源将保存到的文件名（不带路径）。

```csharp
public string ResourceFileName { get; set; }
```

## 评论

此属性允许您重新定义在导出到固定页面 HTML 或 SVG 期间如何生成资源文件名 。

触发事件时，此属性包含由 Aspose.Words 生成的文件名 。您可以更改此属性的值，将资源保存到 不同的文件中。请注意，文件名必须是唯一的。

Aspose.Words 在导出为固定页面 HTML 或 SVG 格式时，会自动为每个资源生成一个唯一的文件名。资源文件名的生成方式取决于您将文档保存为文件还是流。

将文档保存为文件时，生成的资源文件名类似于 &lt;文档基础文件名&gt;.&lt;图像编号&gt;.&lt;扩展名&gt;。

将文档保存到流时，生成的资源文件名类似于 Aspose.Words.&lt;文档 GUID&gt;.&lt;图像编号&gt;.&lt;扩展名&gt;。

`ResourceFileName`必须仅包含文件名而不包含路径。 Aspose.Words 确定保存的路径和`源码`使用文档文件名将 写入固定页面 HTML 或 SVG 的属性，[`ResourcesFolder`](../../htmlfixedsaveoptions/resourcesfolder/) 或[`ResourcesFolder`](../../svgsaveoptions/resourcesfolder/)和[`ResourcesFolderAlias`](../../htmlfixedsaveoptions/resourcesfolderalias/) 或[`ResourcesFolderAlias`](../../svgsaveoptions/resourcesfolderalias/)特性。

[`ResourcesFolder`](../../htmlfixedsaveoptions/resourcesfolder/)[`ResourcesFolder`](../../svgsaveoptions/resourcesfolder/)[`ResourcesFolderAlias`](../../htmlfixedsaveoptions/resourcesfolderalias/)[`ResourcesFolderAlias`](../../svgsaveoptions/resourcesfolderalias/)

## 例子

展示如何使用回调来跟踪将文档转换为 HTML 时创建的外部资源。

```csharp
public void ResourceSavingCallback()
{
    Document doc = new Document(MyDir + "Bullet points with alternative font.docx");

    FontSavingCallback callback = new FontSavingCallback();

    HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions
    {
        ResourceSavingCallback = callback
    };

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

    Console.WriteLine(callback.GetText());
}

private class FontSavingCallback : IResourceSavingCallback
{
    /// <summary>
    /// 当 Aspose.Words 将外部资源保存为固定页面 HTML 或 SVG 时调用。
    /// </summary>
    public void ResourceSaving(ResourceSavingArgs args)
    {
        mText.AppendLine($"Original document URI:\t{args.Document.OriginalFileName}");
        mText.AppendLine($"Resource being saved:\t{args.ResourceFileName}");
        mText.AppendLine($"Full uri after saving:\t{args.ResourceFileUri}\n");
    }

    public string GetText()
    {
        return mText.ToString();
    }

    private readonly StringBuilder mText = new StringBuilder();
}
```

### 也可以看看

* class [ResourceSavingArgs](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
