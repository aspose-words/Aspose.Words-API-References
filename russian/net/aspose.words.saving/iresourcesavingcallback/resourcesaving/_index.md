---
title: IResourceSavingCallback.ResourceSaving
linktitle: ResourceSaving
articleTitle: ResourceSaving
second_title: Aspose.Words для .NET
description: Оптимизируйте обработку документов с помощью метода ResourceSaving в Aspose.Words, улучшающего управление внешними ресурсами для форматов HTML и SVG.
type: docs
weight: 10
url: /ru/net/aspose.words.saving/iresourcesavingcallback/resourcesaving/
---
## IResourceSavingCallback.ResourceSaving method

Вызывается, когда Aspose.Words сохраняет внешний ресурс в форматах HTML или SVG с фиксированной страницей.

```csharp
public void ResourceSaving(ResourceSavingArgs args)
```

## Примеры

Показывает, как использовать обратный вызов для отслеживания внешних ресурсов, созданных при преобразовании документа в HTML.

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
    /// Вызывается, когда Aspose.Words сохраняет внешний ресурс в формате HTML или SVG фиксированной страницы.
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

Показывает, как использовать обратный вызов для печати URI внешних ресурсов, созданных при преобразовании документа в HTML.

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

    // Папка, указанная ResourcesFolderAlias, будет содержать ресурсы вместо ResourcesFolder.
    // Мы должны убедиться, что папка существует, прежде чем потоки смогут поместить в нее свои ресурсы.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

    Console.WriteLine(callback.GetText());

    string[] resourceFiles = Directory.GetFiles(ArtifactsDir + "HtmlFixedResourceFolderAlias");

    Assert.False(Directory.Exists(ArtifactsDir + "HtmlFixedResourceFolder"));
    Assert.AreEqual(6, resourceFiles.Count(f => f.EndsWith(".jpeg") || f.EndsWith(".png") || f.EndsWith(".css")));
}

/// <summary>
/// Подсчитывает и выводит URI ресурсов, содержащихся в, по мере их преобразования в фиксированный HTML.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        // Если мы зададим псевдоним папки в объекте SaveOptions, мы сможем распечатать его отсюда.
        mText.AppendLine($"Resource #{++mSavedResourceCount} \"{args.ResourceFileName}\"");

        string extension = Path.GetExtension(args.ResourceFileName);
        switch (extension)
        {
            case ".ttf":
            case ".woff":
            {
                // По умолчанию «ResourceFileUri» использует системную папку для шрифтов.
                // Чтобы избежать проблем на других платформах, необходимо явно указать путь к шрифтам.
                args.ResourceFileUri = ArtifactsDir + Path.DirectorySeparatorChar + args.ResourceFileName;
                break;
            }
        }

        mText.AppendLine("\t" + args.ResourceFileUri);

        // Если мы указали папку в свойстве "ResourcesFolderAlias",
        // нам также потребуется перенаправить каждый поток, чтобы поместить его ресурс в эту папку.
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

### Смотрите также

* class [ResourceSavingArgs](../../resourcesavingargs/)
* interface [IResourceSavingCallback](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
