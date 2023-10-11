---
title: XamlFlowSaveOptions.ImagesFolderAlias
second_title: Aspose.Words for .NET API 参考
description: XamlFlowSaveOptions 财产. 指定用于构建写入 XAML 文档的图像 URI 的文件夹名称 默认为空字符串
type: docs
weight: 40
url: /zh/net/aspose.words.saving/xamlflowsaveoptions/imagesfolderalias/
---
## XamlFlowSaveOptions.ImagesFolderAlias property

指定用于构建写入 XAML 文档的图像 URI 的文件夹名称。 默认为空字符串。

```csharp
public string ImagesFolderAlias { get; set; }
```

### 评论

当您保存一个[`Document`](../../../aspose.words/document/)在 XAML 格式中，Aspose.Words 需要将文档中嵌入的所有 图像保存为独立文件。[`ImagesFolder`](../imagesfolder/) 允许您指定图像的保存位置`ImagesFolderAlias` 允许指定如何构建图像 URI。

如果`ImagesFolderAlias`不是空字符串，则 XAML 中写入的图像 URI 将是ImagesFolderAlias + &lt;图像文件名&gt;。

如果`ImagesFolderAlias`是一个空字符串，那么写入 到 XAML 的图像 URI 将是ImagesFolder + &lt;图像文件名&gt;。

如果`ImagesFolderAlias`被设定为 '。' （点），那么无论其他选项如何，图像文件名 将被写入 XAML，不带路径。

### 例子

演示如何打印在将文档转换为流格式 .xaml 时创建的链接图像的文件名。

```csharp
public void ImageFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ImageUriPrinter callback = new ImageUriPrinter(ArtifactsDir + "XamlFlowImageFolderAlias");

    // 创建一个“XamlFlowSaveOptions”对象，我们可以将其传递给文档的“Save”方法
    // 修改我们将文档保存为 XAML 保存格式的方式。
    XamlFlowSaveOptions options = new XamlFlowSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFlow, options.SaveFormat);

    // 使用“ImagesFolder”属性在本地文件系统中分配一个文件夹
    // Aspose.Words 将保存文档的所有链接图像。
    options.ImagesFolder = ArtifactsDir + "XamlFlowImageFolder";

    // 使用“ImagesFolderAlias”属性来使用此文件夹
    // 当构造图像 URI 而不是图像文件夹的名称时。
    options.ImagesFolderAlias = ArtifactsDir + "XamlFlowImageFolderAlias";

    options.ImageSavingCallback = callback;

    // 由“ImagesFolderAlias”指定的文件夹需要包含资源，而不是“ImagesFolder”。
    // 我们必须确保该文件夹存在，然后回调的流才能将其资源放入其中。
    Directory.CreateDirectory(options.ImagesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFlowSaveOptions.ImageFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine($"{callback.ImagesFolderAlias}/{resource}");
}

/// <summary>
/// 在父文档转换为流格式 .xaml 时计算并打印图像的文件名。
/// </summary>
private class ImageUriPrinter : IImageSavingCallback
{
    public ImageUriPrinter(string imagesFolderAlias)
    {
        ImagesFolderAlias = imagesFolderAlias;
        Resources = new List<string>();
    }

    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        Resources.Add(args.ImageFileName);

        // 如果我们指定了图像文件夹别名，我们还需要
        // 重定向每个流以将其图像放入别名文件夹中。
        args.ImageStream = new FileStream($"{ImagesFolderAlias}/{args.ImageFileName}", FileMode.Create);
        args.KeepImageStreamOpen = false;
    }

    public string ImagesFolderAlias { get; }
    public List<string> Resources { get; }
}
```

### 也可以看看

* class [XamlFlowSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../xamlflowsaveoptions/)
* 部件 [Aspose.Words](../../../)


