---
title: ResourceSavingArgs.ResourceStream
linktitle: ResourceStream
articleTitle: ResourceStream
second_title: Aspose.Words для .NET
description: ResourceSavingArgs ResourceStream свойство. Позволяет указать поток в котором будет сохранен ресурс на С#.
type: docs
weight: 50
url: /ru/net/aspose.words.saving/resourcesavingargs/resourcestream/
---
## ResourceSavingArgs.ResourceStream property

Позволяет указать поток, в котором будет сохранен ресурс.

```csharp
public Stream ResourceStream { get; set; }
```

## Примечания

Это свойство позволяет сохранять ресурсы в потоки, а не в файлы.

Значение по умолчанию:`нулевой` . Когда это свойство`нулевой` , ресурс будет сохранен в файле, указанном в[`ResourceFileName`](../resourcefilename/) свойство.

С использованием[`IResourceSavingCallback`](../../iresourcesavingcallback/) вы не можете заменить один ресурс другим. Он предназначен только для контроля над местом, где сохранять ресурсы.

## Примеры

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
/// Подсчитывает и печатает URI ресурсов, содержащихся в них, при их преобразовании в фиксированный HTML.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        // Если мы установим псевдоним папки в объекте SaveOptions, мы сможем распечатать его отсюда.
        mText.AppendLine($"Resource #{++mSavedResourceCount} \"{args.ResourceFileName}\"");

        string extension = Path.GetExtension(args.ResourceFileName);
        switch (extension)
        {
            case ".ttf":
            case ".woff":
            {
                // По умолчанию ResourceFileUri использует системную папку для шрифтов.
                // Чтобы избежать проблем на других платформах, необходимо явно указать путь к шрифтам.
                args.ResourceFileUri = ArtifactsDir + Path.DirectorySeparatorChar + args.ResourceFileName;
                break;
            }
        }

        mText.AppendLine("\t" + args.ResourceFileUri);

        // Если мы указали папку в свойстве ResourcesFolderAlias,
        // нам также нужно будет перенаправить каждый поток, чтобы поместить его ресурс в эту папку.
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

* class [ResourceSavingArgs](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
