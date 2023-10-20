---
title: XamlFlowSaveOptions.ImagesFolder
linktitle: ImagesFolder
articleTitle: ImagesFolder
second_title: Aspose.Words для .NET
description: XamlFlowSaveOptions ImagesFolder свойство. Указывает физическую папку в которой сохраняются изображения при экспорте документа в формат XAML. По умолчанию  пустая строка на С#.
type: docs
weight: 30
url: /ru/net/aspose.words.saving/xamlflowsaveoptions/imagesfolder/
---
## XamlFlowSaveOptions.ImagesFolder property

Указывает физическую папку, в которой сохраняются изображения при экспорте документа в формат XAML. По умолчанию — пустая строка.

```csharp
public string ImagesFolder { get; set; }
```

## Примечания

Когда вы сохраняете[`Document`](../../../aspose.words/document/) в формате XAML Aspose.Words необходимо сохранить все изображения , встроенные в документ, как отдельные файлы.`ImagesFolder` позволяет указать, где будут сохраняться изображения и[`ImagesFolderAlias`](../imagesfolderalias/) позволяет указать, как будут создаваться URI изображения.

Если вы сохраняете документ в файл и указываете имя файла, Aspose.Words по умолчанию сохраняет изображения в той же папке, где сохраняется файл документа. Использовать`ImagesFolder` , чтобы переопределить это поведение.

Если вы сохраняете документ в поток, Aspose.Words не имеет папки для сохранения изображений , но все равно необходимо где-то сохранять изображения. В этом случае вам необходимо указать доступную папку в`ImagesFolder` или предоставить собственные потоки через [`ImageSavingCallback`](../imagesavingcallback/) обработчик события.

## Примеры

Показывает, как распечатать имена файлов связанных изображений, созданных при преобразовании документа в потоковую форму .xaml.

```csharp
public void ImageFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ImageUriPrinter callback = new ImageUriPrinter(ArtifactsDir + "XamlFlowImageFolderAlias");

    // Создаем объект «XamlFlowSaveOptions», который мы можем передать методу «Save» документа.
    // чтобы изменить способ сохранения документа в формате сохранения XAML.
    XamlFlowSaveOptions options = new XamlFlowSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFlow, options.SaveFormat);

    // Используйте свойство «ImagesFolder», чтобы назначить папку в локальной файловой системе, в которую
    // Aspose.Words сохранит все связанные изображения документа.
    options.ImagesFolder = ArtifactsDir + "XamlFlowImageFolder";

    // Используйте свойство «ImagesFolderAlias» для использования этой папки
    // при создании URI изображений вместо имени папки изображений.
    options.ImagesFolderAlias = ArtifactsDir + "XamlFlowImageFolderAlias";

    options.ImageSavingCallback = callback;

    // Папка, указанная в «ImagesFolderAlias», должна будет содержать ресурсы вместо «ImagesFolder».
    // Мы должны убедиться, что папка существует, прежде чем потоки обратного вызова смогут поместить в нее свои ресурсы.
    Directory.CreateDirectory(options.ImagesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFlowSaveOptions.ImageFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine($"{callback.ImagesFolderAlias}/{resource}");
}

/// <summary>
/// Подсчитывает и печатает имена файлов изображений, пока их родительский документ преобразуется в потоковую форму .xaml.
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

        // Если бы мы указали псевдоним папки с изображениями, нам также потребовалось бы
        // чтобы перенаправить каждый поток, чтобы поместить его изображение в папку псевдонимов.
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
