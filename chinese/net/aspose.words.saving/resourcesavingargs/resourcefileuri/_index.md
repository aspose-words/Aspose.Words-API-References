---
title: ResourceSavingArgs.ResourceFileUri
linktitle: ResourceFileUri
articleTitle: ResourceFileUri
second_title: Aspose.Words for .NET
description: 探索 ResourceSavingArgs ResourceFileUri 属性，轻松管理和引用文档中的资源文件。立即提升效率！
type: docs
weight: 40
url: /zh/net/aspose.words.saving/resourcesavingargs/resourcefileuri/
---
## ResourceSavingArgs.ResourceFileUri property

获取或设置用于从文档引用资源文件的统一资源标识符 (URI)。

```csharp
public string ResourceFileUri { get; set; }
```

## 评论

此属性允许您更改导出到固定页面 HTML 或 SVG 文档的资源文件的 URI。

Aspose.Words 在导出为固定页面 HTML 或 SVG 格式时，会自动为每个资源文件生成一个 URI。生成的 URI 引用 Aspose.Words 保存的资源文件。但是，如果资源文件要移动到其他位置或保存到流中，则 URI 可能不正确。 此属性允许在这些情况下更正 URI。

当事件触发时，此属性包含由 Aspose.Words 生成的 URI。您可以更改此属性的值，为资源文件提供自定义 URI。

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
