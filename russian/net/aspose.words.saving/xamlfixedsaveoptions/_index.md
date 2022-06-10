---
title: XamlFixedSaveOptions
second_title: Справочник по API Aspose.Words для .NET
description: Может использоваться для указания дополнительных параметров при сохранении документа в форматеXamlFixed.
type: docs
weight: 5360
url: /ru/net/aspose.words.saving/xamlfixedsaveoptions/
---
## XamlFixedSaveOptions class

Может использоваться для указания дополнительных параметров при сохранении документа в форматеXamlFixed.

```csharp
public class XamlFixedSaveOptions : FixedPageSaveOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [XamlFixedSaveOptions](xamlfixedsaveoptions)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts) { get; set; } | Получает или задает логическое значение, указывающее, разрешить ли встраивание шрифтов с контурами PostScript при встраивании шрифтов TrueType в документ после его сохранения. Значение по умолчанию: **false** . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode) { get; set; } | Получает или задает значение, определяющее способ отображения цветов. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo) { get; set; } | Получает или задает пользовательский местный часовой пояс, используемый для полей даты/времени. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate) { get; set; } | Получает или задает путь к шаблону по умолчанию (включая имя файла). Значение по умолчанию для этого свойства: **пустая строка** (Empty). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode) { get; set; } | Получает или задает значение, определяющее способ визуализации 3D-эффектов. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode) { get; set; } | Получает или задает значение, определяющее способ визуализации эффектов DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode) { get; set; } | Получает или задает значение, определяющее способ визуализации фигур DrawingML. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname) { get; set; } | При значении true имя и версия Aspose.Words встраиваются в создаваемые файлы. Значение по умолчанию: **true** . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly) { get; set; } | Получает или задает значение, определяющее, какие форматы документов разрешено отображать с помощью[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping). По умолчанию только формат документаFlatOpcразрешен для сопоставления. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode) { get; set; } | Получает или задает значение, определяющее способ визуализации объектов рукописного ввода (InkML). |
| [JpegQuality](../../aspose.words.saving/fixedpagesaveoptions/jpegquality) { get; set; } | Получает или задает значение, определяющее качество изображений JPEG внутри HTML-документа. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization) { get; set; } | Получает или задает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойства: **false** . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions) { get; set; } | Позволяет указать параметры рендеринга метафайла. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat) { get; set; } | Получает или устанавливает[`NumeralFormat`](../numeralformat)используется для отображения чисел. По умолчанию используются европейские цифры. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput) { get; set; } | Флаг указывает, требуется ли оптимизация вывода. Если этот флаг установлен, лишние вложенные холсты и пустые холсты удаляются, также объединяются соседние глифы с одинаковым форматированием. Примечание. Точность отображения содержимого может быть снижена, если для этого свойства задано значение true. По умолчанию false. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback) { get; set; } | Позволяет управлять сохранением отдельных страниц при экспорте документа в фиксированный формат страницы. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset) { get; set; } | Получает или задает отображаемые страницы. По умолчанию все страницы документа. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat) { get; set; } | Когда` true` , вывод форматируется, где это применимо. Значение по умолчанию: **false** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback) { get; set; } | Вызывается при сохранении документа и принимает данные о ходе сохранения. |
| [ResourceSavingCallback](../../aspose.words.saving/xamlfixedsaveoptions/resourcesavingcallback) { get; set; } | Позволяет управлять сохранением ресурсов (изображений и шрифтов) при экспорте документа в формат фиксированной страницы Xaml. |
| [ResourcesFolder](../../aspose.words.saving/xamlfixedsaveoptions/resourcesfolder) { get; set; } | Указывает физическую папку, в которой сохраняются ресурсы (изображения и шрифты) при экспорте документа в формат фиксированной страницы Xaml. По умолчанию:` null` . |
| [ResourcesFolderAlias](../../aspose.words.saving/xamlfixedsaveoptions/resourcesfolderalias) { get; set; } | Указывает имя папки, используемой для создания URI изображений, записываемых в документ Xaml с фиксированной страницей. По умолчанию:` null` . |
| override [SaveFormat](../../aspose.words.saving/xamlfixedsaveoptions/saveformat) { get; set; } | Указывает формат, в котором будет сохранен документ, если используется этот объект параметров сохранения. Может быть толькоXamlFixed. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder) { get; set; } | Указывает папку для временных файлов, используемых при сохранении в файл DOC или DOCX. По умолчанию это свойство` null` и временные файлы не используются. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty) { get; set; } | Получает или задает значение, определяющее, обновляется ли свойство[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime)перед сохранением. Значение по умолчанию - false; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields) { get; set; } | Получает или задает значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы. Значение по умолчанию для этого свойства: **true** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty) { get; set; } | Получает или задает значение, определяющее, обновляется ли свойство[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted)перед сохранением. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty) { get; set; } | Получает или задает значение, определяющее, обновляется ли свойство[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime)перед сохранением. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent) { get; set; } | Получает или задает значение, определяющее, будет ли содержимое[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag)обновляться перед сохранением. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing) { get; set; } | Получает или задает значение, определяющее, следует ли использовать сглаживание для визуализации. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering) { get; set; } | Получает или задает значение, определяющее, следует ли использовать высококачественные (т.е. медленные) алгоритмы рендеринга. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals)(object) | Определяет, равен ли указанный объект по значению текущему объекту. |

### Примеры

Показывает, как распечатать URI связанных ресурсов, созданных при преобразовании документа в формат .xaml фиксированной формы.

```csharp
public void ResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    ResourceUriPrinter callback = new ResourceUriPrinter();

     // Создаем объект «XamlFixedSaveOptions», который мы можем передать в документ «Сохранить» method
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

         // Если бы мы указали псевдоним папки ресурсов, нам также потребовалось бы 
         // чтобы перенаправить каждый поток, чтобы поместить его ресурс в папку псевдонима.
        args.ResourceStream = new FileStream(args.ResourceFileUri, FileMode.Create);
        args.KeepResourceStreamOpen = false;
    }

    public List<string> Resources { get; }
}
```

### Смотрите также

* class [FixedPageSaveOptions](../fixedpagesaveoptions)
* пространство имен [Aspose.Words.Saving](../../aspose.words.saving)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
