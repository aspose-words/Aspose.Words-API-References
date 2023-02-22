---
title: Class HtmlFixedSaveOptions
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Saving.HtmlFixedSaveOptions сорт. Может использоваться для указания дополнительных параметров при сохранении документа вHtmlFixed формат.
type: docs
weight: 4820
url: /ru/net/aspose.words.saving/htmlfixedsaveoptions/
---
## HtmlFixedSaveOptions class

Может использоваться для указания дополнительных параметров при сохранении документа вHtmlFixed формат.

```csharp
public class HtmlFixedSaveOptions : FixedPageSaveOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [HtmlFixedSaveOptions](htmlfixedsaveoptions/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Возвращает или задает логическое значение, указывающее, разрешать ли встраивание шрифтов с помощью PostScript layouts при встраивании шрифтов TrueType в документ после его сохранения. Значение по умолчанию: **ЛОЖЬ** . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | Получает или задает значение, определяющее способ отображения цветов. |
| [CssClassNamesPrefix](../../aspose.words.saving/htmlfixedsaveoptions/cssclassnamesprefix/) { get; set; } | Указывает префикс, который добавляется ко всем именам классов в файле style.css. Значение по умолчанию:`"оу"` . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Получает или задает пользовательский местный часовой пояс, используемый для полей даты/времени. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Получает или задает путь к шаблону по умолчанию (включая имя файла). Значение по умолчанию для этого свойства: **пустой строки** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Получает или задает значение, определяющее способ визуализации 3D-эффектов. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Получает или задает значение, определяющее способ визуализации эффектов DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Получает или задает значение, определяющее способ визуализации фигур DrawingML. |
| [Encoding](../../aspose.words.saving/htmlfixedsaveoptions/encoding/) { get; set; } | Указывает кодировку, используемую при экспорте в HTML. Значение по умолчанию:`новый UTF8Encoding (истина)` (UTF-8 со спецификацией). |
| [ExportEmbeddedCss](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedcss/) { get; set; } | Указывает, следует ли встраивать CSS (каскадную таблицу стилей) в HTML-документ. |
| [ExportEmbeddedFonts](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedfonts/) { get; set; } | Указывает, должны ли шрифты быть встроены в HTML-документ в формате Base64. Обратите внимание, что установка этого флага может значительно увеличить размер выходного HTML-файла. |
| [ExportEmbeddedImages](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedimages/) { get; set; } | Указывает, следует ли встраивать изображения в HTML-документ в формате Base64. Обратите внимание, что установка этого флага может значительно увеличить размер выходного HTML-файла. |
| [ExportEmbeddedSvg](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedsvg/) { get; set; } | Указывает, следует ли встраивать ресурсы SVG в HTML-документ. Значение по умолчанию:`истинный` . |
| [ExportFormFields](../../aspose.words.saving/htmlfixedsaveoptions/exportformfields/) { get; set; } | Получает или задает индикацию того, экспортируются ли поля формы как интерактивные элементы (как тег 'input'), а не преобразуются в текст или графику. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | При значении true имя и версия Aspose.Words встраиваются в создаваемые файлы. Значение по умолчанию: **истинный** . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly/) { get; set; } | Получает или задает значение, определяющее, какие форматы документов разрешено отображать[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Только по умолчаниюFlatOpc формат документа разрешен для сопоставления. |
| [FontFormat](../../aspose.words.saving/htmlfixedsaveoptions/fontformat/) { get; set; } | Получает или устанавливает[`ExportFontFormat`](../exportfontformat/) используется для экспорта шрифта. Значение по умолчанию:Woff . |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Получает или задает значение, определяющее способ визуализации объектов рукописного ввода (InkML). |
| [JpegQuality](../../aspose.words.saving/fixedpagesaveoptions/jpegquality/) { get; set; } | Получает или задает значение, определяющее качество изображений JPEG внутри HTML-документа. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Получает или задает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойства: **ЛОЖЬ** . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/) { get; set; } | Позволяет указать параметры рендеринга метафайла. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | Получает или устанавливает[`NumeralFormat`](../numeralformat/) используется для отображения цифр. Европейские цифры используются по умолчанию. |
| override [OptimizeOutput](../../aspose.words.saving/htmlfixedsaveoptions/optimizeoutput/) { get; set; } | Флаг указывает, требуется ли оптимизация вывода. этому свойству присвоено значение true. Значение по умолчанию — true. |
| [PageHorizontalAlignment](../../aspose.words.saving/htmlfixedsaveoptions/pagehorizontalalignment/) { get; set; } | Определяет горизонтальное выравнивание страниц в HTML-документе. Значение по умолчанию:`HtmlFixedHorizontalPageAlignment.Center` . |
| [PageMargins](../../aspose.words.saving/htmlfixedsaveoptions/pagemargins/) { get; set; } | Определяет поля вокруг страниц в документе HTML. Значение полей измеряется в пунктах и должно быть равно или больше 0. Значение по умолчанию — 10 пунктов. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Позволяет управлять сохранением отдельных страниц при экспорте документа в фиксированный формат страницы. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset/) { get; set; } | Получает или задает отображаемые страницы. По умолчанию — все страницы документа. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Когда`истинный` , красивые форматы вывода, где это применимо. Значение по умолчанию: **ЛОЖЬ** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Вызывается при сохранении документа и принимает данные о ходе сохранения. |
| [ResourceSavingCallback](../../aspose.words.saving/htmlfixedsaveoptions/resourcesavingcallback/) { get; set; } | Позволяет управлять сохранением ресурсов (изображений, шрифтов и css) при экспорте документа в фиксированный формат страницы Html. |
| [ResourcesFolder](../../aspose.words.saving/htmlfixedsaveoptions/resourcesfolder/) { get; set; } | Указывает физическую папку, в которой сохраняются ресурсы (изображения, шрифты, css) при экспорте документа в формат Html. Значение по умолчанию:`нулевой` . |
| [ResourcesFolderAlias](../../aspose.words.saving/htmlfixedsaveoptions/resourcesfolderalias/) { get; set; } | Указывает имя папки, используемой для создания URI изображений, записываемых в HTML-документ. Значение по умолчанию:`нулевой` . |
| [SaveFontFaceCssSeparately](../../aspose.words.saving/htmlfixedsaveoptions/savefontfacecssseparately/) { get; set; } | Флаг указывает, следует ли помещать правила CSS "@font-face" в отдельный файл "fontFaces.css" при сохранении документа с внешней таблицей стилей (т.[`ExportEmbeddedCss`](./exportembeddedcss/) это`ЛОЖЬ` ). Значение по умолчанию:`ЛОЖЬ` , все правила CSS записываются в один файл "styles.css". |
| override [SaveFormat](../../aspose.words.saving/htmlfixedsaveoptions/saveformat/) { get; set; } | Определяет формат, в котором документ будет сохранен, если используется этот объект параметров сохранения.HtmlFixed . |
| [ShowPageBorder](../../aspose.words.saving/htmlfixedsaveoptions/showpageborder/) { get; set; } | Указывает, следует ли отображать границу вокруг страниц. Значение по умолчанию:`истинный` . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Указывает папку для временных файлов, используемых при сохранении в файл DOC или DOCX. По умолчанию это свойство`нулевой` и никакие временные файлы не используются. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Получает или задает значение, определяющее,[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) свойство обновляется перед сохранением. Значение по умолчанию — false; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Получает или задает значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы. Значение по умолчанию для этого свойства: **истинный** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Получает или задает значение, определяющее,[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) свойство обновляется перед сохранением. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Получает или задает значение, определяющее,[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) свойство обновляется перед сохранением. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent/) { get; set; } | Получает или задает значение, определяющее, будет ли содержимое[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) обновляется перед сохранением. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Получает или задает значение, определяющее, следует ли использовать сглаживание для рендеринга. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Получает или задает значение, определяющее, следует ли использовать высококачественные (т.е. медленные) алгоритмы рендеринга. |
| [UseTargetMachineFonts](../../aspose.words.saving/htmlfixedsaveoptions/usetargetmachinefonts/) { get; set; } | Флаг указывает, должны ли шрифты с целевой машины использоваться для отображения документа. Если для этого флага установлено значение true,[`FontFormat`](./fontformat/) а также[`ExportEmbeddedFonts`](./exportembeddedfonts/)свойства не действуют, также[`ResourceSavingCallback`](./resourcesavingcallback/) не срабатывает для шрифтов. Значение по умолчанию — false. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(object) | Определяет, равен ли указанный объект по значению текущему объекту. |

### Примеры

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

    // Папка, указанная в ResourcesFolderAlias, будет содержать ресурсы вместо ResourcesFolder.
    // Мы должны убедиться, что папка существует, прежде чем потоки смогут поместить в нее свои ресурсы.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

    Console.WriteLine(callback.GetText());

    string[] resourceFiles = Directory.GetFiles(ArtifactsDir + "HtmlFixedResourceFolderAlias");

    Assert.False(Directory.Exists(ArtifactsDir + "HtmlFixedResourceFolder"));
    Assert.AreEqual(6, resourceFiles.Count(f => f.EndsWith(".jpeg") || f.EndsWith(".png") || f.EndsWith(".css")));
}

/// <summary>
/// Подсчитывает и печатает URI ресурсов, содержащихся в по мере их преобразования в фиксированный HTML.
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
                // По умолчанию 'ResourceFileUri' использует системную папку для шрифтов.
                // Чтобы избежать проблем на других платформах, вы должны явно указать путь к шрифтам.
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

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)


