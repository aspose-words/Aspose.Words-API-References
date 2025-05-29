---
title: ResourceType Enum
linktitle: ResourceType
articleTitle: ResourceType
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.ResourceType 枚举，实现高效的资源管理。使用丰富的加载选项增强您的文档处理能力。
type: docs
weight: 4160
url: /zh/net/aspose.words.loading/resourcetype/
---
## ResourceType enumeration

已加载资源的类型。

```csharp
public enum ResourceType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Image | `0` | 图像. |
| Font | `1` | 字体. |
| CssStyleSheet | `2` | CSS 样式表。 |
| Document | `3` | 文档. |

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
