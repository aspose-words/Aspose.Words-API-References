---
title: HtmlSaveOptions
second_title: Справочник по API Aspose.Words для .NET
description: Может использоваться для указания дополнительных параметров при сохранении документа вHtml MhtmlилиEpubформат.
type: docs
weight: 4800
url: /ru/net/aspose.words.saving/htmlsaveoptions/
---
## HtmlSaveOptions class

Может использоваться для указания дополнительных параметров при сохранении документа вHtml, MhtmlилиEpubформат.

```csharp
public class HtmlSaveOptions : SaveOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [HtmlSaveOptions](htmlsaveoptions#constructor)() | Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа в файлеHtml. |
| [HtmlSaveOptions](htmlsaveoptions#constructor_1)(SaveFormat) | Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа в файлеHtml,Mhtml илиEpubформат . |

## Характеристики

| Имя | Описание |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts) { get; set; } | Получает или задает логическое значение, указывающее, разрешить ли встраивание шрифтов с контурами PostScript при встраивании шрифтов TrueType в документ после его сохранения. Значение по умолчанию: **false** . |
| [AllowNegativeIndent](../../aspose.words.saving/htmlsaveoptions/allownegativeindent) { get; set; } | Указывает, нормализуются ли отрицательные левый и правый отступы абзацев при сохранении в HTML, MHTML или EPUB. Значение по умолчанию:` false` . |
| [CssClassNamePrefix](../../aspose.words.saving/htmlsaveoptions/cssclassnameprefix) { get; set; } | Указывает префикс, который добавляется ко всем именам классов CSS. Значение по умолчанию — пустая строка, а сгенерированные имена классов CSS не имеют общего префикса. |
| [CssSavingCallback](../../aspose.words.saving/htmlsaveoptions/csssavingcallback) { get; set; } | Позволяет управлять сохранением стилей CSS при сохранении документа в формате HTML, MHTML или EPUB. |
| [CssStyleSheetFileName](../../aspose.words.saving/htmlsaveoptions/cssstylesheetfilename) { get; set; } | Указывает путь и имя файла каскадной таблицы стилей (CSS), записываемого при экспорте документа в HTML. По умолчанию пустая строка. |
| [CssStyleSheetType](../../aspose.words.saving/htmlsaveoptions/cssstylesheettype) { get; set; } | Указывает, как стили CSS (каскадные таблицы стилей) экспортируются в HTML, MHTML или EPUB. Значение по умолчанию:Inlineдля HTML/MHTML и Externalдля EPUB. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo) { get; set; } | Получает или задает пользовательский местный часовой пояс, используемый для полей даты/времени. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate) { get; set; } | Получает или задает путь к шаблону по умолчанию (включая имя файла). Значение по умолчанию для этого свойства: **пустая строка** (Empty). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode) { get; set; } | Получает или задает значение, определяющее способ визуализации 3D-эффектов. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode) { get; set; } | Получает или задает значение, определяющее способ визуализации эффектов DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode) { get; set; } | Получает или задает значение, определяющее способ визуализации фигур DrawingML. |
| [DocumentPartSavingCallback](../../aspose.words.saving/htmlsaveoptions/documentpartsavingcallback) { get; set; } | Позволяет управлять сохранением частей документа при сохранении документа в формате HTML или EPUB. |
| [DocumentSplitCriteria](../../aspose.words.saving/htmlsaveoptions/documentsplitcriteria) { get; set; } | Указывает, как документ должен быть разделен при сохранении вHtml илиEpubформат. По умолчанию:Noneдля HTML и HeadingParagraphдля EPUB. |
| [DocumentSplitHeadingLevel](../../aspose.words.saving/htmlsaveoptions/documentsplitheadinglevel) { get; set; } | Задает максимальный уровень заголовков, на котором можно разделить документ. Значение по умолчанию:` 2` . |
| [Encoding](../../aspose.words.saving/htmlsaveoptions/encoding) { get; set; } | Указывает кодировку, используемую при экспорте в HTML, MHTML или EPUB. Значение по умолчанию:` new UTF8Encoding(false)` (UTF-8 без спецификации). |
| [EpubNavigationMapLevel](../../aspose.words.saving/htmlsaveoptions/epubnavigationmaplevel) { get; set; } | Указывает максимальный уровень заголовков, заполняемых навигационной картой при экспорте в формат IDPF EPUB. Значение по умолчанию:` 3` . |
| [ExportCidUrlsForMhtmlResources](../../aspose.words.saving/htmlsaveoptions/exportcidurlsformhtmlresources) { get; set; } | Указывает, следует ли использовать URL-адреса CID (Content-ID) для ссылки на ресурсы (изображения, шрифты, CSS), включенные в документы MHTML . Значение по умолчанию:` false` . |
| [ExportDocumentProperties](../../aspose.words.saving/htmlsaveoptions/exportdocumentproperties) { get; set; } | Указывает, экспортировать ли встроенные и пользовательские свойства документа в HTML, MHTML или EPUB. Значение по умолчанию:` false` . |
| [ExportDropDownFormFieldAsText](../../aspose.words.saving/htmlsaveoptions/exportdropdownformfieldastext) { get; set; } | Управляет способом сохранения полей раскрывающихся форм в HTML или MHTML. Значение по умолчанию:` false` . |
| [ExportFontResources](../../aspose.words.saving/htmlsaveoptions/exportfontresources) { get; set; } | Указывает, следует ли экспортировать ресурсы шрифта в HTML, MHTML или EPUB. По умолчанию:` false` . |
| [ExportFontsAsBase64](../../aspose.words.saving/htmlsaveoptions/exportfontsasbase64) { get; set; } | Указывает, следует ли встраивать ресурсы шрифтов в HTML в кодировке Base64. По умолчанию:` false` . |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname) { get; set; } | При значении true имя и версия Aspose.Words встраиваются в создаваемые файлы. Значение по умолчанию: **true** . |
| [ExportHeadersFootersMode](../../aspose.words.saving/htmlsaveoptions/exportheadersfootersmode) { get; set; } | Указывает, как верхние и нижние колонтитулы выводятся в HTML, MHTML или EPUB. Значение по умолчанию:PerSectionдля HTML/MHTML иNoneдля EPUB. |
| [ExportImagesAsBase64](../../aspose.words.saving/htmlsaveoptions/exportimagesasbase64) { get; set; } | Указывает, сохраняются ли изображения в формате Base64 в выходной HTML, MHTML или EPUB. По умолчанию:` false` . |
| [ExportLanguageInformation](../../aspose.words.saving/htmlsaveoptions/exportlanguageinformation) { get; set; } | Указывает, экспортируется ли языковая информация в HTML, MHTML или EPUB. По умолчанию:` false` . |
| [ExportListLabels](../../aspose.words.saving/htmlsaveoptions/exportlistlabels) { get; set; } | Управляет выводом меток списков в HTML, MHTML или EPUB. Значение по умолчанию:Auto. |
| [ExportOriginalUrlForLinkedImages](../../aspose.words.saving/htmlsaveoptions/exportoriginalurlforlinkedimages) { get; set; } | Указывает, следует ли использовать исходный URL-адрес в качестве URL-адреса связанных изображений. Значение по умолчанию:` false` . |
| [ExportPageMargins](../../aspose.words.saving/htmlsaveoptions/exportpagemargins) { get; set; } | Указывает, экспортируются ли поля страницы в HTML, MHTML или EPUB. По умолчанию:` false` . |
| [ExportPageSetup](../../aspose.words.saving/htmlsaveoptions/exportpagesetup) { get; set; } | Указывает, экспортируются ли настройки страницы в HTML, MHTML или EPUB. По умолчанию:` false` . |
| [ExportRelativeFontSize](../../aspose.words.saving/htmlsaveoptions/exportrelativefontsize) { get; set; } | Указывает, должны ли размеры шрифта выводиться в относительных единицах при сохранении в HTML, MHTML или EPUB. По умолчанию:` false` . |
| [ExportRoundtripInformation](../../aspose.words.saving/htmlsaveoptions/exportroundtripinformation) { get; set; } | Указывает, следует ли записывать информацию о пути туда и обратно при сохранении в HTML, MHTML или EPUB. Значение по умолчанию:` true` для HTML и` false` для MHTML и EPUB. |
| [ExportShapesAsSvg](../../aspose.words.saving/htmlsaveoptions/exportshapesassvg) { get; set; } | Контролирует, будут ли узлы[`Shape`](../../aspose.words.drawing/shape)преобразовываться в изображения SVG при сохранении в HTML, MHTML или EPUB. Значение по умолчанию:` false` . |
| [ExportTextInputFormFieldAsText](../../aspose.words.saving/htmlsaveoptions/exporttextinputformfieldastext) { get; set; } | Управляет тем, как поля формы ввода текста сохраняются в HTML или MHTML. Значение по умолчанию:` false` . |
| [ExportTocPageNumbers](../../aspose.words.saving/htmlsaveoptions/exporttocpagenumbers) { get; set; } | Указывает, записывать ли номера страниц в оглавление при сохранении HTML, MHTML и EPUB. Значение по умолчанию:` false` . |
| [ExportXhtmlTransitional](../../aspose.words.saving/htmlsaveoptions/exportxhtmltransitional) { get; set; } | Указывает, следует ли записывать объявление DOCTYPE при сохранении в HTML или MHTML. Когда` true` , записывает объявление DOCTYPE в документ перед корневым элементом. Значение по умолчанию:` false` . При сохранении в EPUB или HTML5 (Html5) всегда записывается объявление DOCTYPE . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly) { get; set; } | Получает или задает значение, определяющее, какие форматы документов разрешено отображать с помощью[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping). По умолчанию только формат документаFlatOpcразрешен для сопоставления. |
| [FontResourcesSubsettingSizeThreshold](../../aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold) { get; set; } | Управляет тем, какие ресурсы шрифтов нуждаются в подразделении при сохранении в HTML, MHTML или EPUB. По умолчанию:` 0` . |
| [FontSavingCallback](../../aspose.words.saving/htmlsaveoptions/fontsavingcallback) { get; set; } | Позволяет управлять сохранением шрифтов при сохранении документа в формате HTML, MHTML или EPUB. |
| [FontsFolder](../../aspose.words.saving/htmlsaveoptions/fontsfolder) { get; set; } | Указывает физическую папку, в которой сохраняются шрифты при экспорте документа в HTML. По умолчанию пустая строка. |
| [FontsFolderAlias](../../aspose.words.saving/htmlsaveoptions/fontsfolderalias) { get; set; } | Задает имя папки, используемой для создания URI шрифтов, записываемых в документ HTML. По умолчанию пустая строка. |
| [HtmlVersion](../../aspose.words.saving/htmlsaveoptions/htmlversion) { get; set; } | Указывает версию стандарта HTML, которую следует использовать при сохранении документа в формате HTML или MHTML. Значение по умолчанию:Xhtml. |
| [ImageResolution](../../aspose.words.saving/htmlsaveoptions/imageresolution) { get; set; } | Указывает выходное разрешение для изображений при экспорте в HTML, MHTML или EPUB. По умолчанию:` 96 dpi` . |
| [ImageSavingCallback](../../aspose.words.saving/htmlsaveoptions/imagesavingcallback) { get; set; } | Позволяет управлять сохранением изображений при сохранении документа в формате HTML, MHTML или EPUB. |
| [ImagesFolder](../../aspose.words.saving/htmlsaveoptions/imagesfolder) { get; set; } | Указывает физическую папку, в которой сохраняются изображения при экспорте документа в формат HTML. По умолчанию пустая строка. |
| [ImagesFolderAlias](../../aspose.words.saving/htmlsaveoptions/imagesfolderalias) { get; set; } | Указывает имя папки, используемой для построения URI изображений, записываемых в документ HTML. По умолчанию пустая строка. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode) { get; set; } | Получает или задает значение, определяющее способ визуализации объектов рукописного ввода (InkML). |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization) { get; set; } | Получает или задает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойства: **false** . |
| [MetafileFormat](../../aspose.words.saving/htmlsaveoptions/metafileformat) { get; set; } | Указывает, в каком формате сохраняются метафайлы при экспорте в HTML, MHTML или EPUB. Значение по умолчанию:Png, что означает, что метафайлы визуализируются в растровые изображения PNG. |
| [OfficeMathOutputMode](../../aspose.words.saving/htmlsaveoptions/officemathoutputmode) { get; set; } | Управляет экспортом объектов OfficeMath в HTML, MHTML или EPUB. Значение по умолчанию:` HtmlOfficeMathOutputMode.Image` . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat) { get; set; } | Когда` true` , вывод форматируется, где это применимо. Значение по умолчанию: **false** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback) { get; set; } | Вызывается при сохранении документа и принимает данные о ходе сохранения. |
| [ResolveFontNames](../../aspose.words.saving/htmlsaveoptions/resolvefontnames) { get; set; } | Указывает, разрешаются ли имена семейств шрифтов, используемые в документе, и заменяются в соответствии с [`FontSettings`](../../aspose.words/document/fontsettings)при записи в HTML-форматы. |
| [ResourceFolder](../../aspose.words.saving/htmlsaveoptions/resourcefolder) { get; set; } | Указывает физическую папку, в которой сохраняются все ресурсы, такие как изображения, шрифты и внешний CSS, когда документ экспортируется в HTML. По умолчанию это пустая строка. |
| [ResourceFolderAlias](../../aspose.words.saving/htmlsaveoptions/resourcefolderalias) { get; set; } | Указывает имя папки, используемой для построения URI всех ресурсов, записываемых в документ HTML. По умолчанию пустая строка. |
| override [SaveFormat](../../aspose.words.saving/htmlsaveoptions/saveformat) { get; set; } | Указывает формат, в котором будет сохранен документ, если используется этот объект параметров сохранения. Может бытьHtml,Mhtml илиEpub. |
| [ScaleImageToShapeSize](../../aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize) { get; set; } | Указывает, масштабируются ли изображения с помощью Aspose.Words до размера ограничивающей фигуры при экспорте в HTML, MHTML или EPUB. Значение по умолчанию:` true` . |
| [TableWidthOutputMode](../../aspose.words.saving/htmlsaveoptions/tablewidthoutputmode) { get; set; } | Контролирует, как ширина таблицы, строки и ячейки экспортируется в HTML, MHTML или EPUB. Значение по умолчанию:All. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder) { get; set; } | Указывает папку для временных файлов, используемых при сохранении в файл DOC или DOCX. По умолчанию это свойство` null` и временные файлы не используются. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty) { get; set; } | Получает или задает значение, определяющее, обновляется ли свойство[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime)перед сохранением. Значение по умолчанию - false; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields) { get; set; } | Получает или задает значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы. Значение по умолчанию для этого свойства: **true** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty) { get; set; } | Получает или задает значение, определяющее, обновляется ли свойство[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted)перед сохранением. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty) { get; set; } | Получает или задает значение, определяющее, обновляется ли свойство[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime)перед сохранением. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent) { get; set; } | Получает или задает значение, определяющее, будет ли содержимое[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag)обновляться перед сохранением. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing) { get; set; } | Получает или задает значение, определяющее, следует ли использовать сглаживание для визуализации. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering) { get; set; } | Получает или задает значение, определяющее, следует ли использовать высококачественные (т.е. медленные) алгоритмы рендеринга. |

### Примеры

Показывает, как указать папку для хранения связанных изображений после сохранения в формате .html.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

     // Создаем объект «HtmlFixedSaveOptions», который мы можем передать в метод «Сохранить» документа method
     // чтобы изменить способ преобразования документа в HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

     // Если мы сохраним документ нормально, будет один вывод HTML
     // документ со всем содержимым исходного документа.
    // Установите для свойства "DocumentSplitCriteria" значение "DocumentSplitCriteria.SectionBreak" to
     // сохраняем наш документ в несколько файлов HTML: по одному на каждый раздел.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

     // Назначаем пользовательский обратный вызов свойству «DocumentPartSavingCallback», чтобы изменить логику сохранения части документа.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

     // Если мы преобразуем документ, содержащий изображения, в html, мы получим один html-файл, который ссылается на несколько изображений.
     // Каждое изображение будет в виде файла в локальной файловой системе.
     // Существует также обратный вызов, который может настроить имя и местоположение файловой системы для каждого изображения.
    options.ImageSavingCallback = new SavedImageRename(outFileName);

    doc.Save(ArtifactsDir + outFileName, options);
}

/// <summary>
 /// Задает пользовательские имена файлов для выходных документов, на которые операция сохранения разбивает документ.
/// </summary>
private class SavedDocumentPartRename : IDocumentPartSavingCallback
{
    public SavedDocumentPartRename(string outFileName, DocumentSplitCriteria documentSplitCriteria)
    {
        mOutFileName = outFileName;
        mDocumentSplitCriteria = documentSplitCriteria;
    }

    void IDocumentPartSavingCallback.DocumentPartSaving(DocumentPartSavingArgs args)
    {
         // Мы можем получить доступ ко всему исходному документу через свойство "Документ".
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        string partType = string.Empty;

        switch (mDocumentSplitCriteria)
        {
            case DocumentSplitCriteria.PageBreak:
                partType = "Page";
                break;
            case DocumentSplitCriteria.ColumnBreak:
                partType = "Column";
                break;
            case DocumentSplitCriteria.SectionBreak:
                partType = "Section";
                break;
            case DocumentSplitCriteria.HeadingParagraph:
                partType = "Paragraph from heading";
                break;
        }

        string partFileName = $"{mOutFileName} part {++mCount}, of type {partType}{Path.GetExtension(args.DocumentPartFileName)}";

         // Ниже приведены два способа указать, где Aspose.Words будет сохранять каждую часть документа.
         // 1 - Установить имя файла для выходного файла части: 
        args.DocumentPartFileName = partFileName;

         // 2 - Создать пользовательский поток для файла выходной части: 
        args.DocumentPartStream = new FileStream(ArtifactsDir + partFileName, FileMode.Create);

        Assert.True(args.DocumentPartStream.CanWrite);
        Assert.False(args.KeepDocumentPartStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
    private readonly DocumentSplitCriteria mDocumentSplitCriteria;
}

/// <summary>
/// Устанавливает пользовательские имена файлов для файлов изображений, которые создаются при преобразовании HTML.
/// </summary>
public class SavedImageRename : IImageSavingCallback
{
    public SavedImageRename(string outFileName)
    {
        mOutFileName = outFileName;
    }

    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        string imageFileName = $"{mOutFileName} shape {++mCount}, of type {args.CurrentShape.ShapeType}{Path.GetExtension(args.ImageFileName)}";

         // Ниже приведены два способа указать, где Aspose.Words будет сохранять каждую часть документа.
         // 1 - Установить имя файла выходного изображения: 
        args.ImageFileName = imageFileName;

         // 2 - Создать пользовательский поток для выходного файла изображения: 
        args.ImageStream = new FileStream(ArtifactsDir + imageFileName, FileMode.Create);

        Assert.True(args.ImageStream.CanWrite);
        Assert.True(args.IsImageAvailable);
        Assert.False(args.KeepImageStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
}
```

Показывает, как использовать определенную кодировку при сохранении документа в формате .epub.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

     // Создаем объект «HtmlFixedSaveOptions», который мы можем передать в метод «Сохранить» документа method
     // чтобы изменить способ преобразования документа в HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

     // Если мы сохраним документ нормально, будет один вывод HTML
     // документ со всем содержимым исходного документа.
    // Установите для свойства "DocumentSplitCriteria" значение "DocumentSplitCriteria.SectionBreak" to
     // сохраняем наш документ в несколько файлов HTML: по одному на каждый раздел.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

     // Назначаем пользовательский обратный вызов свойству «DocumentPartSavingCallback», чтобы изменить логику сохранения части документа.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

     // Если мы преобразуем документ, содержащий изображения, в html, мы получим один html-файл, который ссылается на несколько изображений.
     // Каждое изображение будет в виде файла в локальной файловой системе.
     // Существует также обратный вызов, который может настроить имя и местоположение файловой системы для каждого изображения.
    options.ImageSavingCallback = new SavedImageRename(outFileName);

    doc.Save(ArtifactsDir + outFileName, options);
}

/// <summary>
 /// Задает пользовательские имена файлов для выходных документов, на которые операция сохранения разбивает документ.
/// </summary>
private class SavedDocumentPartRename : IDocumentPartSavingCallback
{
    public SavedDocumentPartRename(string outFileName, DocumentSplitCriteria documentSplitCriteria)
    {
        mOutFileName = outFileName;
        mDocumentSplitCriteria = documentSplitCriteria;
    }

    void IDocumentPartSavingCallback.DocumentPartSaving(DocumentPartSavingArgs args)
    {
         // Мы можем получить доступ ко всему исходному документу через свойство "Документ".
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        string partType = string.Empty;

        switch (mDocumentSplitCriteria)
        {
            case DocumentSplitCriteria.PageBreak:
                partType = "Page";
                break;
            case DocumentSplitCriteria.ColumnBreak:
                partType = "Column";
                break;
            case DocumentSplitCriteria.SectionBreak:
                partType = "Section";
                break;
            case DocumentSplitCriteria.HeadingParagraph:
                partType = "Paragraph from heading";
                break;
        }

        string partFileName = $"{mOutFileName} part {++mCount}, of type {partType}{Path.GetExtension(args.DocumentPartFileName)}";

         // Ниже приведены два способа указать, где Aspose.Words будет сохранять каждую часть документа.
         // 1 - Установить имя файла для выходного файла части: 
        args.DocumentPartFileName = partFileName;

         // 2 - Создать пользовательский поток для файла выходной части: 
        args.DocumentPartStream = new FileStream(ArtifactsDir + partFileName, FileMode.Create);

        Assert.True(args.DocumentPartStream.CanWrite);
        Assert.False(args.KeepDocumentPartStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
    private readonly DocumentSplitCriteria mDocumentSplitCriteria;
}

/// <summary>
/// Устанавливает пользовательские имена файлов для файлов изображений, которые создаются при преобразовании HTML.
/// </summary>
public class SavedImageRename : IImageSavingCallback
{
    public SavedImageRename(string outFileName)
    {
        mOutFileName = outFileName;
    }

    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        string imageFileName = $"{mOutFileName} shape {++mCount}, of type {args.CurrentShape.ShapeType}{Path.GetExtension(args.ImageFileName)}";

         // Ниже приведены два способа указать, где Aspose.Words будет сохранять каждую часть документа.
         // 1 - Установить имя файла выходного изображения: 
        args.ImageFileName = imageFileName;

         // 2 - Создать пользовательский поток для выходного файла изображения: 
        args.ImageStream = new FileStream(ArtifactsDir + imageFileName, FileMode.Create);

        Assert.True(args.ImageStream.CanWrite);
        Assert.True(args.IsImageAvailable);
        Assert.False(args.KeepImageStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
}
```

Показывает, как разделить документ на части и сохранить их.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

     // Создаем объект «HtmlFixedSaveOptions», который мы можем передать в метод «Сохранить» документа method
     // чтобы изменить способ преобразования документа в HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

     // Если мы сохраним документ нормально, будет один вывод HTML
     // документ со всем содержимым исходного документа.
    // Установите для свойства "DocumentSplitCriteria" значение "DocumentSplitCriteria.SectionBreak" to
     // сохраняем наш документ в несколько файлов HTML: по одному на каждый раздел.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

     // Назначаем пользовательский обратный вызов свойству «DocumentPartSavingCallback», чтобы изменить логику сохранения части документа.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

     // Если мы преобразуем документ, содержащий изображения, в html, мы получим один html-файл, который ссылается на несколько изображений.
     // Каждое изображение будет в виде файла в локальной файловой системе.
     // Существует также обратный вызов, который может настроить имя и местоположение файловой системы для каждого изображения.
    options.ImageSavingCallback = new SavedImageRename(outFileName);

    doc.Save(ArtifactsDir + outFileName, options);
}

/// <summary>
 /// Задает пользовательские имена файлов для выходных документов, на которые операция сохранения разбивает документ.
/// </summary>
private class SavedDocumentPartRename : IDocumentPartSavingCallback
{
    public SavedDocumentPartRename(string outFileName, DocumentSplitCriteria documentSplitCriteria)
    {
        mOutFileName = outFileName;
        mDocumentSplitCriteria = documentSplitCriteria;
    }

    void IDocumentPartSavingCallback.DocumentPartSaving(DocumentPartSavingArgs args)
    {
         // Мы можем получить доступ ко всему исходному документу через свойство "Документ".
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        string partType = string.Empty;

        switch (mDocumentSplitCriteria)
        {
            case DocumentSplitCriteria.PageBreak:
                partType = "Page";
                break;
            case DocumentSplitCriteria.ColumnBreak:
                partType = "Column";
                break;
            case DocumentSplitCriteria.SectionBreak:
                partType = "Section";
                break;
            case DocumentSplitCriteria.HeadingParagraph:
                partType = "Paragraph from heading";
                break;
        }

        string partFileName = $"{mOutFileName} part {++mCount}, of type {partType}{Path.GetExtension(args.DocumentPartFileName)}";

         // Ниже приведены два способа указать, где Aspose.Words будет сохранять каждую часть документа.
         // 1 - Установить имя файла для выходного файла части: 
        args.DocumentPartFileName = partFileName;

         // 2 - Создать пользовательский поток для файла выходной части: 
        args.DocumentPartStream = new FileStream(ArtifactsDir + partFileName, FileMode.Create);

        Assert.True(args.DocumentPartStream.CanWrite);
        Assert.False(args.KeepDocumentPartStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
    private readonly DocumentSplitCriteria mDocumentSplitCriteria;
}

/// <summary>
/// Устанавливает пользовательские имена файлов для файлов изображений, которые создаются при преобразовании HTML.
/// </summary>
public class SavedImageRename : IImageSavingCallback
{
    public SavedImageRename(string outFileName)
    {
        mOutFileName = outFileName;
    }

    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        string imageFileName = $"{mOutFileName} shape {++mCount}, of type {args.CurrentShape.ShapeType}{Path.GetExtension(args.ImageFileName)}";

         // Ниже приведены два способа указать, где Aspose.Words будет сохранять каждую часть документа.
         // 1 - Установить имя файла выходного изображения: 
        args.ImageFileName = imageFileName;

         // 2 - Создать пользовательский поток для выходного файла изображения: 
        args.ImageStream = new FileStream(ArtifactsDir + imageFileName, FileMode.Create);

        Assert.True(args.ImageStream.CanWrite);
        Assert.True(args.IsImageAvailable);
        Assert.False(args.KeepImageStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
}
```

### Смотрите также

* class [SaveOptions](../saveoptions)
* namespace [Aspose.Words.Saving](../../aspose.words.saving)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
