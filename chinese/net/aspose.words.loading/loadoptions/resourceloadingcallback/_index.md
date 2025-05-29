---
title: LoadOptions.ResourceLoadingCallback
linktitle: ResourceLoadingCallback
articleTitle: ResourceLoadingCallback
second_title: Aspose.Words for .NET
description: 使用 LoadOptions 的 ResourceLoadingCallback 优化文档导入。无缝控制图片和样式表等外部资源的加载。
type: docs
weight: 140
url: /zh/net/aspose.words.loading/loadoptions/resourceloadingcallback/
---
## LoadOptions.ResourceLoadingCallback property

允许控制从 HTML、MHTML 导入文档时如何加载外部资源（图像、样式表）。

```csharp
public IResourceLoadingCallback ResourceLoadingCallback { get; set; }
```

## 例子

展示如何在加载 Html 文档时处理外部资源。

```csharp
public void LoadOptionsCallback()
{
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.ResourceLoadingCallback = new HtmlLinkedResourceLoadingCallback();

    // 当我们加载文档时，我们的回调将处理链接的资源，例如 CSS 样式表和图像。
    Document doc = new Document(MyDir + "Images.html", loadOptions);
    doc.Save(ArtifactsDir + "LoadOptions.LoadOptionsCallback.pdf");
}

/// <summary>
/// 打印所有外部样式表的文件名并替换已加载的 html 文档的所有图像。
/// </summary>
private class HtmlLinkedResourceLoadingCallback : IResourceLoadingCallback
{
    public ResourceLoadingAction ResourceLoading(ResourceLoadingArgs args)
    {
        switch (args.ResourceType)
        {
            case ResourceType.CssStyleSheet:
                Console.WriteLine($"External CSS Stylesheet found upon loading: {args.OriginalUri}");
                return ResourceLoadingAction.Default;
            case ResourceType.Image:
                Console.WriteLine($"External Image found upon loading: {args.OriginalUri}");

                const string newImageFilename = "Logo.jpg";
                Console.WriteLine($"\tImage will be substituted with: {newImageFilename}");

                Image newImage = Image.FromFile(ImageDir + newImageFilename);

                ImageConverter converter = new ImageConverter();
                byte[] imageBytes = (byte[])converter.ConvertTo(newImage, typeof(byte[]));
                args.SetData(imageBytes);

                return ResourceLoadingAction.UserProvided;
        }

        return ResourceLoadingAction.Default;
    }
}
```

### 也可以看看

* interface [IResourceLoadingCallback](../../iresourceloadingcallback/)
* class [LoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
