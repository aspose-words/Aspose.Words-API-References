---
title: XamlFlowSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
articleTitle: ImagesFolderAlias
second_title: Aspose.Words for .NET
description: 探索 XamlFlowSaveOptions 的 ImagesFolderAlias 属性，自定义 XAML 文档中的图像 URI 路径。轻松增强您的项目！
type: docs
weight: 40
url: /zh/net/aspose.words.saving/xamlflowsaveoptions/imagesfolderalias/
---
## XamlFlowSaveOptions.ImagesFolderAlias property

指定用于构建写入 XAML 文档的图像 URI 的文件夹的名称。 默认值为空字符串。

```csharp
public string ImagesFolderAlias { get; set; }
```

## 评论

当你保存[`Document`](../../../aspose.words/document/)在XAML格式中，Aspose.Words需要将文档中嵌入的所有 图像保存为独立文件。[`ImagesFolder`](../imagesfolder/) 允许您指定图像的保存位置，并且`ImagesFolderAlias` 允许指定如何构建图像 URI。

如果`ImagesFolderAlias`不是空字符串，那么 XAML 中的图像 URI written 将是ImagesFolderAlias + &lt;图像文件名&gt;。

如果`ImagesFolderAlias`是空字符串，则写入 XAML 的图像 URI 将是ImagesFolder + &lt;图像文件名&gt;。

如果`ImagesFolderAlias`设置为“.”（点），那么无论其他选项如何，图像文件名 都将写入XAML而不带路径。

## 例子

展示如何打印将文档转换为流式 .xaml 时创建的链接图像的文件名。

```csharp
public void ImageFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ImageUriPrinter callback = new ImageUriPrinter(ArtifactsDir + "XamlFlowImageFolderAlias");

    // 创建一个“XamlFlowSaveOptions”对象，我们可以将其传递给文档的“Save”方法
    // 修改我们将文档保存为 XAML 保存格式的方式。
    XamlFlowSaveOptions options = new XamlFlowSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFlow, options.SaveFormat);

    // 使用“ImagesFolder”属性在本地文件系统中分配一个文件夹，
    // Aspose.Words 将保存文档的所有链接图像。
    options.ImagesFolder = ArtifactsDir + "XamlFlowImageFolder";

    // 使用“ImagesFolderAlias”属性来使用此文件夹
    // 构建图像 URI 时，而不是图像文件夹的名称。
    options.ImagesFolderAlias = ArtifactsDir + "XamlFlowImageFolderAlias";

    options.ImageSavingCallback = callback;

    // 由“ImagesFolderAlias”指定的文件夹将需要包含资源，而不是“ImagesFolder”。
    // 我们必须确保该文件夹存在，然后回调的流才能将其资源放入其中。
    Directory.CreateDirectory(options.ImagesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFlowSaveOptions.ImageFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine($"{callback.ImagesFolderAlias}/{resource}");
}

/// <summary>
/// 在将图像的父文档转换为流形式 .xaml 时，计算并打印图像的文件名。
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
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
