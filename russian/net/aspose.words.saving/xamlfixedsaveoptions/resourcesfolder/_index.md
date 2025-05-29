---
title: XamlFixedSaveOptions.ResourcesFolder
linktitle: ResourcesFolder
articleTitle: ResourcesFolder
second_title: Aspose.Words для .NET
description: Узнайте, как свойство XamlFixedSaveOptions ResourcesFolder улучшает экспорт документов, определяя, где хранятся изображения и шрифты в формате Xaml.
type: docs
weight: 30
url: /ru/net/aspose.words.saving/xamlfixedsaveoptions/resourcesfolder/
---
## XamlFixedSaveOptions.ResourcesFolder property

Указывает физическую папку, в которой сохраняются ресурсы (изображения и шрифты) при экспорте документа в формат XAML с фиксированной страницей. Значение по умолчанию:`нулевой` .

```csharp
public string ResourcesFolder { get; set; }
```

## Примечания

Когда вы сохраняете[`Document`](../../../aspose.words/document/) в формате XAML с фиксированной страницей Aspose.Words необходимо сохранить все изображения x000d, встроенные в документ, как отдельные файлы.`ResourcesFolder` позволяет указать, где будут сохранены изображения и[`ResourcesFolderAlias`](../resourcesfolderalias/) позволяет указать, как будут формироваться URI изображений.

Если вы сохраняете документ в файл и указываете имя файла, Aspose.Words по умолчанию сохраняет изображения the в той же папке, где сохранен файл документа. Используйте`ResourcesFolder` для переопределения этого поведения.

Если вы сохраняете документ в поток, Aspose.Words не имеет папки, куда можно сохранять изображения, , но все равно должен сохранять изображения где-то. В этом случае вам нужно указать доступную папку с помощью`ResourcesFolder` свойство

## Примеры

Показывает, как распечатать URI связанных ресурсов, созданных при преобразовании документа в фиксированный формат .xaml.

```csharp
public void ResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    ResourceUriPrinter callback = new ResourceUriPrinter();

    // Создаем объект "XamlFixedSaveOptions", который можно передать методу "Save" документа
    // чтобы изменить способ сохранения документа в формате XAML.
    XamlFixedSaveOptions options = new XamlFixedSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFixed, options.SaveFormat);

    // Используйте свойство "ResourcesFolder", чтобы назначить папку в локальной файловой системе, в которую
    // Aspose.Words сохранит все связанные ресурсы документа, такие как изображения и шрифты.
    options.ResourcesFolder = ArtifactsDir + "XamlFixedResourceFolder";

    // Используйте свойство "ResourcesFolderAlias" для использования этой папки
    // при построении URI изображений вместо имени папки ресурсов.
    options.ResourcesFolderAlias = ArtifactsDir + "XamlFixedFolderAlias";

    options.ResourceSavingCallback = callback;

    // Папка, указанная в «ResourcesFolderAlias», должна содержать ресурсы вместо «ResourcesFolder».
    // Мы должны убедиться, что папка существует, прежде чем потоки обратного вызова смогут поместить в нее свои ресурсы.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFixedSaveOptions.ResourceFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine(resource);
}

/// <summary>
/// Подсчитывает и печатает URI ресурсов, созданных во время преобразования в фиксированный .xaml.
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

        // Если бы мы указали псевдоним папки ресурсов, нам также понадобилось бы
        // для перенаправления каждого потока для помещения его ресурса в папку псевдонима.
        args.ResourceStream = new FileStream(args.ResourceFileUri, FileMode.Create);
        args.KeepResourceStreamOpen = false;
    }

    public List<string> Resources { get; }
}
```

### Смотрите также

* class [XamlFixedSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
