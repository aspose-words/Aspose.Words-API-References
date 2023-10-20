---
title: ResourceSavingArgs Class
linktitle: ResourceSavingArgs
articleTitle: ResourceSavingArgs
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Saving.ResourceSavingArgs 班级. 提供数据ResourceSaving事件 在 C#.
type: docs
weight: 5560
url: /zh/net/aspose.words.saving/resourcesavingargs/
---
## ResourceSavingArgs class

提供数据[`ResourceSaving`](../iresourcesavingcallback/resourcesaving/)事件.

要了解更多信息，请访问[保存文档](https://docs.aspose.com/words/net/save-a-document/)文档文章。

```csharp
public class ResourceSavingArgs
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Document](../../aspose.words.saving/resourcesavingargs/document/) { get; } | 获取当前正在保存的文档对象。 |
| [KeepResourceStreamOpen](../../aspose.words.saving/resourcesavingargs/keepresourcestreamopen/) { get; set; } | 指定 Aspose.Words 在保存资源后是否应保持流打开或关闭它。 |
| [ResourceFileName](../../aspose.words.saving/resourcesavingargs/resourcefilename/) { get; set; } | 获取或设置资源将保存到的文件名（不带路径）。 |
| [ResourceFileUri](../../aspose.words.saving/resourcesavingargs/resourcefileuri/) { get; set; } | 获取或设置用于从文档引用资源文件的统一资源标识符 (URI)。 |
| [ResourceStream](../../aspose.words.saving/resourcesavingargs/resourcestream/) { get; set; } | 允许指定资源将保存到的流。 |

## 评论

默认情况下，当 Aspose.Words 将文档保存到固定页面 HTML 或 SVG 时，它会将每个资源保存到 一个单独的文件中。 Aspose.Words 使用文档文件名和唯一编号为文档中找到的每个资源生成唯一的文件名 。

`ResourceSavingArgs`允许重新定义如何生成资源文件名，或者通过提供您自己的流对象 完全避免将资源保存到文件中。

要应用您自己的逻辑来生成资源文件名，请使用 [`ResourceFileName`](./resourcefilename/)财产。

要将资源保存到流而不是文件中，请使用[`ResourceStream`](./resourcestream/)财产。

## 例子

演示如何使用回调来跟踪将文档转换为 HTML 时创建的外部资源。

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
    /// 当 Aspose.Words 将外部资源保存到固定页面 HTML 或 SVG 时调用。
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

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
