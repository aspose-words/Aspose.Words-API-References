---
title: XamlFixedSaveOptions.ResourcesFolderAlias
linktitle: ResourcesFolderAlias
articleTitle: ResourcesFolderAlias
second_title: 用于 .NET 的 Aspose.Words
description: XamlFixedSaveOptions ResourcesFolderAlias 财产. 指定用于构造写入固定页面 Xaml 文档中的图像 URI 的文件夹的名称 默认为无效的 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words.saving/xamlfixedsaveoptions/resourcesfolderalias/
---
## XamlFixedSaveOptions.ResourcesFolderAlias property

指定用于构造写入固定页面 Xaml 文档中的图像 URI 的文件夹的名称。 默认为`无效的`.

```csharp
public string ResourcesFolderAlias { get; set; }
```

## 评论

当您保存一个[`Document`](../../../aspose.words/document/)在固定页面 Xaml 格式中，Aspose.Words 需要将文档中嵌入的 all 图像保存为独立文件。[`ResourcesFolder`](../resourcesfolder/) 允许您指定图像的保存位置`ResourcesFolderAlias` 允许指定如何构建图像 URI。

## 例子

演示如何打印在将文档转换为固定格式 .xaml 时创建的链接资源的 URI。

```csharp
public void ResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    ResourceUriPrinter callback = new ResourceUriPrinter();

    // 创建一个“XamlFixedSaveOptions”对象，我们可以将其传递给文档的“Save”方法
    // 修改我们将文档保存为 XAML 保存格式的方式。
    XamlFixedSaveOptions options = new XamlFixedSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFixed, options.SaveFormat);

    // 使用“ResourcesFolder”属性在本地文件系统中分配一个文件夹
    // Aspose.Words 将保存所有文档的链接资源，例如图像和字体。
    options.ResourcesFolder = ArtifactsDir + "XamlFixedResourceFolder";

    // 使用“ResourcesFolderAlias”属性来使用此文件夹
    // 当构造图像 URI 而不是资源文件夹的名称时。
    options.ResourcesFolderAlias = ArtifactsDir + "XamlFixedFolderAlias";

    options.ResourceSavingCallback = callback;

    // 由“ResourcesFolderAlias”指定的文件夹需要包含资源，而不是“ResourcesFolder”。
    // 我们必须确保该文件夹存在，然后回调的流才能将其资源放入其中。
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFixedSaveOptions.ResourceFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine(resource);
}

/// <summary>
/// 计算并打印转换为固定 .xaml 期间创建的资源的 URI。
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    public ResourceUriPrinter()
    {
        Resources = new List<string>();
    }

    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        Resources.Add($"Resource \"{args.ResourceFileName}\"\n\t{args.ResourceFileUri}");

        // 如果我们指定了资源文件夹别名，我们还需要
        // 重定向每个流以将其资源放入别名文件夹中。
        args.ResourceStream = new FileStream(args.ResourceFileUri, FileMode.Create);
        args.KeepResourceStreamOpen = false;
    }

    public List<string> Resources { get; }
}
```

### 也可以看看

* class [XamlFixedSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
