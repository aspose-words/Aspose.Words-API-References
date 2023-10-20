---
title: HtmlFixedSaveOptions.ResourcesFolder
linktitle: ResourcesFolder
articleTitle: ResourcesFolder
second_title: 用于 .NET 的 Aspose.Words
description: HtmlFixedSaveOptions ResourcesFolder 财产. 指定将文档导出为 Html 格式时保存资源图像字体css的物理文件夹 默认为无效的 在 C#.
type: docs
weight: 140
url: /zh/net/aspose.words.saving/htmlfixedsaveoptions/resourcesfolder/
---
## HtmlFixedSaveOptions.ResourcesFolder property

指定将文档导出为 Html 格式时保存资源（图像、字体、css）的物理文件夹。 默认为`无效的`.

```csharp
public string ResourcesFolder { get; set; }
```

## 评论

仅当以下情况时才有效[`ExportEmbeddedImages`](../exportembeddedimages/)财产是`错误的`。

当您保存一个[`Document`](../../../aspose.words/document/)在 Html 格式中，Aspose.Words 需要将文档中嵌入的 all 图像保存为独立文件。`ResourcesFolder` 允许您指定图像的保存位置[`ResourcesFolderAlias`](../resourcesfolderalias/) 允许指定如何构建图像 URI。

如果将文档保存到文件中并提供文件名，默认情况下，Aspose.Words 会将 图像保存在保存文档文件的同一文件夹中。使用`ResourcesFolder` 覆盖此行为。

如果将文档保存到流中，Aspose.Words 没有保存图像的文件夹 ，但仍需要将图像保存在某个位置。在这种情况下，您需要使用以下命令指定可访问的文件夹 `ResourcesFolder`财产

## 例子

演示如何使用回调来打印在将文档转换为 HTML 时创建的外部资源的 URI。

```csharp
public void HtmlFixedResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ResourceUriPrinter callback = new ResourceUriPrinter();

    HtmlFixedSaveOptions options = new HtmlFixedSaveOptions
    {
        SaveFormat = SaveFormat.HtmlFixed,
        ExportEmbeddedImages = false,
        ResourcesFolder = ArtifactsDir + "HtmlFixedResourceFolder",
        ResourcesFolderAlias = ArtifactsDir + "HtmlFixedResourceFolderAlias",
        ShowPageBorder = false,
        ResourceSavingCallback = callback
    };

    // 由 ResourcesFolderAlias 指定的文件夹将包含资源而不是 ResourcesFolder。
    // 我们必须确保该文件夹存在，然后流才能将其资源放入其中。
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

    Console.WriteLine(callback.GetText());

    string[] resourceFiles = Directory.GetFiles(ArtifactsDir + "HtmlFixedResourceFolderAlias");

    Assert.False(Directory.Exists(ArtifactsDir + "HtmlFixedResourceFolder"));
    Assert.AreEqual(6, resourceFiles.Count(f => f.EndsWith(".jpeg") || f.EndsWith(".png") || f.EndsWith(".css")));
}

/// <summary>
/// 计算并打印 包含的资源的 URI，因为它们被转换为固定的 HTML。
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        // 如果我们在 SaveOptions 对象中设置文件夹别名，我们将能够从这里打印它。
        mText.AppendLine($"Resource #{++mSavedResourceCount} \"{args.ResourceFileName}\"");

        string extension = Path.GetExtension(args.ResourceFileName);
        switch (extension)
        {
            case ".ttf":
            case ".woff":
            {
                // 默认情况下，“ResourceFileUri”使用系统文件夹来存储字体。
                // 为了避免在其他平台上出现问题，您必须显式指定字体的路径。
                args.ResourceFileUri = ArtifactsDir + Path.DirectorySeparatorChar + args.ResourceFileName;
                break;
            }
        }

        mText.AppendLine("\t" + args.ResourceFileUri);

        // 如果我们在“ResourcesFolderAlias”属性中指定了一个文件夹，
        // 我们还需要重定向每个流以将其资源放入该文件夹中。
        args.ResourceStream = new FileStream(args.ResourceFileUri, FileMode.Create);
        args.KeepResourceStreamOpen = false;
    }

    public string GetText()
    {
        return mText.ToString();
    }

    private int mSavedResourceCount;
    private readonly StringBuilder mText = new StringBuilder();
}
```

### 也可以看看

* class [HtmlFixedSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
