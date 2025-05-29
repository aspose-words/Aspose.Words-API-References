---
title: XamlFlowSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
articleTitle: ImagesFolderAlias
second_title: Aspose.Words для .NET
description: Откройте для себя свойство XamlFlowSaveOptions' ImagesFolderAlias для настройки путей URI изображений в документах XAML. Улучшайте свои проекты с легкостью!
type: docs
weight: 40
url: /ru/net/aspose.words.saving/xamlflowsaveoptions/imagesfolderalias/
---
## XamlFlowSaveOptions.ImagesFolderAlias property

Указывает имя папки, используемой для создания URI изображений, записанных в документ XAML. По умолчанию — пустая строка.

```csharp
public string ImagesFolderAlias { get; set; }
```

## Примечания

Когда вы сохраняете[`Document`](../../../aspose.words/document/) в формате XAML Aspose.Words необходимо сохранить все изображения , встроенные в документ, как отдельные файлы.[`ImagesFolder`](../imagesfolder/) позволяет указать, где будут сохранены изображения и`ImagesFolderAlias` позволяет указать, как будут формироваться URI изображений.

Если`ImagesFolderAlias` не пустая строка, то URI изображенияwritten в XAML будетImagesFolderAlias + &lt;имя файла изображения&gt;.

Если`ImagesFolderAlias` пустая строка, то URI изображения, записанный как в XAML, будетImagesFolder + &lt;имя файла изображения&gt;.

Если`ImagesFolderAlias` установлено значение «.» (точка), то имя файла изображения будет записано в XAML без пути независимо от других параметров.

## Примеры

Показывает, как распечатать имена файлов связанных изображений, созданных при преобразовании документа в формат .xaml с потоковой формой.

```csharp
public void ImageFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ImageUriPrinter callback = new ImageUriPrinter(ArtifactsDir + "XamlFlowImageFolderAlias");

    // Создаем объект "XamlFlowSaveOptions", который можно передать методу "Save" документа
    // чтобы изменить способ сохранения документа в формате XAML.
    XamlFlowSaveOptions options = new XamlFlowSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFlow, options.SaveFormat);

    // Используйте свойство "ImagesFolder", чтобы назначить папку в локальной файловой системе, в которую
    // Aspose.Words сохранит все связанные изображения документа.
    options.ImagesFolder = ArtifactsDir + "XamlFlowImageFolder";

    // Используйте свойство "ImagesFolderAlias" для использования этой папки
    // при построении URI изображений вместо имени папки с изображениями.
    options.ImagesFolderAlias = ArtifactsDir + "XamlFlowImageFolderAlias";

    options.ImageSavingCallback = callback;

    // Папка, указанная в «ImagesFolderAlias», должна содержать ресурсы вместо «ImagesFolder».
    // Мы должны убедиться, что папка существует, прежде чем потоки обратного вызова смогут поместить в нее свои ресурсы.
    Directory.CreateDirectory(options.ImagesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFlowSaveOptions.ImageFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine($"{callback.ImagesFolderAlias}/{resource}");
}

/// <summary>
/// Подсчитывает и печатает имена файлов изображений, пока их родительский документ преобразуется в потоковый формат .xaml.
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

        // Если бы мы указали псевдоним папки с изображениями, нам также понадобилось бы
        // для перенаправления каждого потока для помещения его изображения в папку псевдонима.
        args.ImageStream = new FileStream($"{ImagesFolderAlias}/{args.ImageFileName}", FileMode.Create);
        args.KeepImageStreamOpen = false;
    }

    public string ImagesFolderAlias { get; }
    public List<string> Resources { get; }
}
```

### Смотрите также

* class [XamlFlowSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
