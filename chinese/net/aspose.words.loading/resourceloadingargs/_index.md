---
title: ResourceLoadingArgs Class
linktitle: ResourceLoadingArgs
articleTitle: ResourceLoadingArgs
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Loading.ResourceLoadingArgs 类，旨在提升您应用程序中的资源加载效率。立即解锁无缝集成！
type: docs
weight: 4150
url: /zh/net/aspose.words.loading/resourceloadingargs/
---
## ResourceLoadingArgs class

为[`ResourceLoading`](../iresourceloadingcallback/resourceloading/)方法.

```csharp
public class ResourceLoadingArgs
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [OriginalUri](../../aspose.words.loading/resourceloadingargs/originaluri/) { get; } | 导入文档中指定的资源的原始 URI。 |
| [ResourceType](../../aspose.words.loading/resourceloadingargs/resourcetype/) { get; } | 资源类型。 |
| [Uri](../../aspose.words.loading/resourceloadingargs/uri/) { get; set; } | 用于下载的资源的 URI 如果[`ResourceLoading`](../iresourceloadingcallback/resourceloading/) 返回Default。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [SetData](../../aspose.words.loading/resourceloadingargs/setdata/)(*byte[]*) | 设置用户提供的资源数据，如果[`ResourceLoading`](../iresourceloadingcallback/resourceloading/) 返回UserProvided. |

## 例子

展示如何自定义将外部资源加载到文档中的过程。

```csharp
public void ResourceLoadingCallback()
{
    Document doc = new Document();
    doc.ResourceLoadingCallback = new ImageNameHandler();

    DocumentBuilder builder = new DocumentBuilder(doc);

    // 图像通常使用 URI 或字节数组插入。
    // 每个资源加载实例都会调用我们的回调的 ResourceLoading 方法。
    builder.InsertImage("Google logo");
    builder.InsertImage("Aspose logo");
    builder.InsertImage("Watermark");

    Assert.AreEqual(3, doc.GetChildNodes(NodeType.Shape, true).Count);

    doc.Save(ArtifactsDir + "DocumentBase.ResourceLoadingCallback.docx");
}

/// <summary>
/// 允许我们使用预定义的简写（而不是 URI）将图像加载到文档中。
/// 这将把图像加载逻辑与文档构造的其余部分分开。
/// </summary>
private class ImageNameHandler : IResourceLoadingCallback
{
    public ResourceLoadingAction ResourceLoading(ResourceLoadingArgs args)
    {
        // 如果此回调在加载图像时遇到图像简写之一，
        // 它将为每个定义的简写应用唯一的逻辑，而不是将其视为 URI。
        if (args.ResourceType == ResourceType.Image)
            switch (args.OriginalUri)
            {
                case "Google logo":
                    using (WebClient webClient = new WebClient())
                    {
                        args.SetData(webClient.DownloadData("http://www.google.com/images/logos/ps_logo2.png");
                    }

                    return ResourceLoadingAction.UserProvided;

                case "Aspose logo":
                    args.SetData(File.ReadAllBytes(ImageDir + "Logo.jpg"));

                    return ResourceLoadingAction.UserProvided;

                case "Watermark":
                    args.SetData(File.ReadAllBytes(ImageDir + "Transparent background logo.png"));

                    return ResourceLoadingAction.UserProvided;
            }

        return ResourceLoadingAction.Default;
    }
}
```

### 也可以看看

* 命名空间 [Aspose.Words.Loading](../../aspose.words.loading/)
* 部件 [Aspose.Words](../../)
