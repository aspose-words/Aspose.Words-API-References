---
title: XamlFlowSaveOptions Class
linktitle: XamlFlowSaveOptions
articleTitle: XamlFlowSaveOptions
second_title: Aspose.Words для .NET
description: Откройте для себя Aspose.Words.Saving.XamlFlowSaveOptions для улучшенного сохранения документов в форматах XamlFlow. Разблокируйте расширенные функции для бесшовной интеграции!
type: docs
weight: 6500
url: /ru/net/aspose.words.saving/xamlflowsaveoptions/
---
## XamlFlowSaveOptions class

Может использоваться для указания дополнительных параметров при сохранении документа в XamlFlow илиXamlFlowPack формат.

Чтобы узнать больше, посетите[Укажите параметры сохранения](https://docs.aspose.com/words/net/specify-save-options/) документальная статья.

```csharp
public class XamlFlowSaveOptions : SaveOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [XamlFlowSaveOptions](xamlflowsaveoptions/#constructor)() | Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа вXamlFlow формат. |
| [XamlFlowSaveOptions](xamlflowsaveoptions/#constructor_1)(*[SaveFormat](../../aspose.words/saveformat/)*) | Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа вXamlFlow илиXamlFlowPack формат. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Возвращает или задает логическое значение, указывающее, разрешать ли встраивание шрифтов с контурами PostScript при встраивании шрифтов TrueType в документ при его сохранении. Значение по умолчанию:`ЛОЖЬ` . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Возвращает или задает пользовательский локальный часовой пояс, используемый для полей даты/времени. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Возвращает или задает путь к шаблону по умолчанию (включая имя файла). Значение по умолчанию для этого свойства:**пустая строка** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Возвращает или задает значение, определяющее способ визуализации 3D-эффектов. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Возвращает или задает значение, определяющее способ визуализации эффектов DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Возвращает или задает значение, определяющее способ визуализации фигур DrawingML. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Когда`истинный` , приводит к внедрению имени и версии Aspose.Words в создаваемые файлы. Значение по умолчанию:`истинный` . |
| [ImageSavingCallback](../../aspose.words.saving/xamlflowsaveoptions/imagesavingcallback/) { get; set; } | Позволяет управлять сохранением изображений при сохранении документа в XAML. |
| [ImagesFolder](../../aspose.words.saving/xamlflowsaveoptions/imagesfolder/) { get; set; } | Указывает физическую папку, в которой сохраняются изображения при экспорте документа в формат XAML. По умолчанию — пустая строка. |
| [ImagesFolderAlias](../../aspose.words.saving/xamlflowsaveoptions/imagesfolderalias/) { get; set; } | Указывает имя папки, используемой для создания URI изображений, записанных в документ XAML. По умолчанию — пустая строка. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Возвращает или задает значение, определяющее способ визуализации объектов рукописного ввода (InkML). |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Возвращает или задает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойства:`ЛОЖЬ` . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Когда`истинный` , красивые форматы вывода, где это применимо. Значение по умолчанию:`ЛОЖЬ` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Вызывается во время сохранения документа и принимает данные о ходе сохранения. |
| [ReplaceBackslashWithYenSign](../../aspose.words.saving/xamlflowsaveoptions/replacebackslashwithyensign/) { get; set; } | Указывает, следует ли заменять символы обратной косой черты на знаки йены. Значение по умолчанию:`ЛОЖЬ` . |
| override [SaveFormat](../../aspose.words.saving/xamlflowsaveoptions/saveformat/) { get; set; } | Указывает формат, в котором будет сохранен документ, если используется этот объект параметров сохранения. Может быть толькоXamlFlow . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Указывает папку для временных файлов, используемых при сохранении в файл DOC или DOCX. По умолчанию это свойство`нулевой` и временные файлы не используются. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Определяет, будут ли изменяться атрибуты шрифта в соответствии с используемым кодом символа. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Возвращает или задает значение, определяющее, является ли[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) свойство обновляется перед сохранением. Значение по умолчанию:`ЛОЖЬ` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Возвращает или задает значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы. Значение по умолчанию для этого свойства:`истинный` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Возвращает или задает значение, определяющее, является ли[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) свойство обновляется перед сохранением. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Возвращает или задает значение, определяющее, является ли[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) свойство обновляется перед сохранением. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Возвращает или задает значение, определяющее, следует ли использовать сглаживание при рендеринге. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Возвращает или задает значение, определяющее, следует ли использовать высококачественные (т. е. медленные) алгоритмы рендеринга. |

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

* class [SaveOptions](../saveoptions/)
* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
