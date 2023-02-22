---
title: XamlFixedSaveOptions.ResourcesFolder
second_title: Справочник по API Aspose.Words для .NET
description: XamlFixedSaveOptions свойство. Указывает физическую папку в которой сохраняются ресурсы изображения и шрифты при экспорте документа в формат фиксированной страницы Xaml. Значение по умолчаниюнулевой .
type: docs
weight: 30
url: /ru/net/aspose.words.saving/xamlfixedsaveoptions/resourcesfolder/
---
## XamlFixedSaveOptions.ResourcesFolder property

Указывает физическую папку, в которой сохраняются ресурсы (изображения и шрифты) при экспорте документа в формат фиксированной страницы Xaml. Значение по умолчанию:`нулевой` .

```csharp
public string ResourcesFolder { get; set; }
```

### Примечания

Когда вы сохраняете[`Document`](../../../aspose.words/document/) в формате фиксированной страницы Xaml Aspose.Words необходимо сохранить все изображения , встроенные в документ, как отдельные файлы.`ResourcesFolder` позволяет указать, где изображения будут сохранены и[`ResourcesFolderAlias`](../resourcesfolderalias/) позволяет указать, как будут создаваться URI изображения.

Если вы сохраняете документ в файл и указываете имя файла, Aspose.Words по умолчанию сохраняет изображения в той же папке, где сохранен файл документа. Использовать`ResourcesFolder` , чтобы переопределить это поведение.

Если вы сохраняете документ в поток, Aspose.Words не имеет папки для сохранения изображений, , но все равно нужно куда-то сохранять изображения. В этом случае вам нужно указать доступную папку с помощью`ResourcesFolder` имущество

### Примеры

Показывает, как распечатать URI связанных ресурсов, созданных при преобразовании документа в XAML фиксированной формы.

```csharp
public void ResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    ResourceUriPrinter callback = new ResourceUriPrinter();

    // Создаем объект "XamlFixedSaveOptions", который мы можем передать методу "Сохранить" документа
    // чтобы изменить способ сохранения документа в формате сохранения XAML.
    XamlFixedSaveOptions options = new XamlFixedSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFixed, options.SaveFormat);

    // Используйте свойство "ResourcesFolder", чтобы назначить папку в локальной файловой системе, в которую
    // Aspose.Words сохранит все связанные ресурсы документа, такие как изображения и шрифты.
    options.ResourcesFolder = ArtifactsDir + "XamlFixedResourceFolder";

    // Используйте свойство "ResourcesFolderAlias", чтобы использовать эту папку
    // при построении URI изображения вместо имени папки ресурсов.
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

        // Если бы мы указали псевдоним папки ресурсов, нам также понадобился бы
        // чтобы перенаправить каждый поток, чтобы поместить его ресурс в папку псевдонима.
        args.ResourceStream = new FileStream(args.ResourceFileUri, FileMode.Create);
        args.KeepResourceStreamOpen = false;
    }

    public List<string> Resources { get; }
}
```

### Смотрите также

* class [XamlFixedSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../xamlfixedsaveoptions/)
* сборка [Aspose.Words](../../../)


