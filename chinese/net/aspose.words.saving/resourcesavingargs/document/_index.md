---
title: ResourceSavingArgs.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words for .NET
description: 发现 ResourceSavingArgs Document 属性来访问正在保存的当前文档对象，从而提高您的工作流程效率。
type: docs
weight: 10
url: /zh/net/aspose.words.saving/resourcesavingargs/document/
---
## ResourceSavingArgs.Document property

获取当前正在保存的文档对象。

```csharp
public Document Document { get; }
```

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

* class [Document](../../../aspose.words/document/)
* class [ResourceSavingArgs](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
