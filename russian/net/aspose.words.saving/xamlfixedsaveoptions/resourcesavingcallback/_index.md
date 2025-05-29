---
title: XamlFixedSaveOptions.ResourceSavingCallback
linktitle: ResourceSavingCallback
articleTitle: ResourceSavingCallback
second_title: Aspose.Words для .NET
description: Оптимизируйте экспорт документов с помощью XamlFixedSaveOptions ResourceSavingCallback. Управляйте сохранением изображений и шрифтов для повышения эффективности формата XAML.
type: docs
weight: 20
url: /ru/net/aspose.words.saving/xamlfixedsaveoptions/resourcesavingcallback/
---
## XamlFixedSaveOptions.ResourceSavingCallback property

Позволяет контролировать, как сохраняются ресурсы (изображения и шрифты) при экспорте документа в формат XAML с фиксированной страницей.

```csharp
public IResourceSavingCallback ResourceSavingCallback { get; set; }
```

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

* interface [IResourceSavingCallback](../../iresourcesavingcallback/)
* class [XamlFixedSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
