---
title: HtmlSaveOptions Class
linktitle: HtmlSaveOptions
articleTitle: HtmlSaveOptions
second_title: Aspose.Words для .NET
description: Откройте для себя Aspose.Words.Saving.HtmlSaveOptions, чтобы улучшить сохранение документов в форматах HTML, MHTML, EPUB, AZW3 и MOBI с помощью настраиваемых параметров.
type: docs
weight: 5860
url: /ru/net/aspose.words.saving/htmlsaveoptions/
---
## HtmlSaveOptions class

Может использоваться для указания дополнительных параметров при сохранении документа в Html ,Mhtml ,Epub , Azw3 илиMobi формат.

Чтобы узнать больше, посетите[Укажите параметры сохранения](https://docs.aspose.com/words/net/specify-save-options/) документальная статья.

```csharp
public class HtmlSaveOptions : SaveOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [HtmlSaveOptions](htmlsaveoptions/#constructor)() | Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа вHtml формат. |
| [HtmlSaveOptions](htmlsaveoptions/#constructor_1)(*[SaveFormat](../../aspose.words/saveformat/)*) | Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа вHtml ,Mhtml ,Epub , Azw3 илиMobi формат. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Возвращает или задает логическое значение, указывающее, разрешать ли встраивание шрифтов с контурами PostScript при встраивании шрифтов TrueType в документ при его сохранении. Значение по умолчанию:`ЛОЖЬ` . |
| [AllowNegativeIndent](../../aspose.words.saving/htmlsaveoptions/allownegativeindent/) { get; set; } | Указывает, нормализуются ли отрицательные левые и правые отступы абзацев при сохранении в HTML, MHTML или EPUB. Значение по умолчанию:`ЛОЖЬ` . |
| [CssClassNamePrefix](../../aspose.words.saving/htmlsaveoptions/cssclassnameprefix/) { get; set; } | Указывает префикс, который добавляется ко всем именам классов CSS. Значением по умолчанию является пустая строка, а сгенерированные имена классов CSS не имеют общего префикса. |
| [CssSavingCallback](../../aspose.words.saving/htmlsaveoptions/csssavingcallback/) { get; set; } | Позволяет контролировать сохранение стилей CSS при сохранении документа в формате HTML, MHTML или EPUB. |
| [CssStyleSheetFileName](../../aspose.words.saving/htmlsaveoptions/cssstylesheetfilename/) { get; set; } | Указывает путь и имя файла каскадной таблицы стилей (CSS), записанного при экспорте документа в HTML. По умолчанию — пустая строка. |
| [CssStyleSheetType](../../aspose.words.saving/htmlsaveoptions/cssstylesheettype/) { get; set; } | Указывает, как стили CSS (каскадные таблицы стилей) экспортируются в HTML, MHTML или EPUB. Значение по умолчанию:Inline для HTML/MHTML и External для EPUB. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Возвращает или задает пользовательский локальный часовой пояс, используемый для полей даты/времени. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Возвращает или задает путь к шаблону по умолчанию (включая имя файла). Значение по умолчанию для этого свойства:**пустая строка** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Возвращает или задает значение, определяющее способ визуализации 3D-эффектов. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Возвращает или задает значение, определяющее способ визуализации эффектов DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Возвращает или задает значение, определяющее способ визуализации фигур DrawingML. |
| [DocumentPartSavingCallback](../../aspose.words.saving/htmlsaveoptions/documentpartsavingcallback/) { get; set; } | Позволяет контролировать, как сохраняются части документа при сохранении документа в формате HTML или EPUB. |
| [DocumentSplitCriteria](../../aspose.words.saving/htmlsaveoptions/documentsplitcriteria/) { get; set; } | Указывает, как следует разделить документ при сохранении вHtml , Epub илиAzw3 format. Значение по умолчанию:None для HTML и HeadingParagraph для EPUB и AZW3. |
| [DocumentSplitHeadingLevel](../../aspose.words.saving/htmlsaveoptions/documentsplitheadinglevel/) { get; set; } | Указывает максимальный уровень заголовков, по которому следует разделить документ. Значение по умолчанию:`2` . |
| [Encoding](../../aspose.words.saving/htmlsaveoptions/encoding/) { get; set; } | Указывает кодировку, используемую при экспорте в HTML, MHTML или EPUB. Значение по умолчанию:`новая кодировка UTF8(false)` (UTF-8 без BOM). |
| [ExportCidUrlsForMhtmlResources](../../aspose.words.saving/htmlsaveoptions/exportcidurlsformhtmlresources/) { get; set; } | Указывает, следует ли использовать URL-адреса CID (Content-ID) для ссылок на ресурсы (изображения, шрифты, CSS), включенные в документы MHTML . Значение по умолчанию:`ЛОЖЬ` . |
| [ExportDocumentProperties](../../aspose.words.saving/htmlsaveoptions/exportdocumentproperties/) { get; set; } | Указывает, следует ли экспортировать встроенные и пользовательские свойства документа в HTML, MHTML или EPUB. Значение по умолчанию:`ЛОЖЬ` . |
| [ExportDropDownFormFieldAsText](../../aspose.words.saving/htmlsaveoptions/exportdropdownformfieldastext/) { get; set; } | Управляет сохранением полей раскрывающихся форм в HTML или MHTML. Значение по умолчанию:`ЛОЖЬ` . |
| [ExportFontResources](../../aspose.words.saving/htmlsaveoptions/exportfontresources/) { get; set; } | Указывает, следует ли экспортировать ресурсы шрифта в HTML, MHTML или EPUB. Значение по умолчанию:`ЛОЖЬ` . |
| [ExportFontsAsBase64](../../aspose.words.saving/htmlsaveoptions/exportfontsasbase64/) { get; set; } | Указывает, следует ли встраивать ресурсы шрифтов в HTML в кодировке Base64. Значение по умолчанию:`ЛОЖЬ` . |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Когда`истинный` , приводит к внедрению имени и версии Aspose.Words в создаваемые файлы. Значение по умолчанию:`истинный` . |
| [ExportHeadersFootersMode](../../aspose.words.saving/htmlsaveoptions/exportheadersfootersmode/) { get; set; } | Указывает, как верхние и нижние колонтитулы выводятся в HTML, MHTML или EPUB. Значение по умолчанию:PerSection для HTML/MHTML иNone для EPUB. |
| [ExportImagesAsBase64](../../aspose.words.saving/htmlsaveoptions/exportimagesasbase64/) { get; set; } | Указывает, сохраняются ли изображения в формате Base64 для выходных файлов HTML, MHTML или EPUB. Значение по умолчанию:`ЛОЖЬ` . |
| [ExportLanguageInformation](../../aspose.words.saving/htmlsaveoptions/exportlanguageinformation/) { get; set; } | Указывает, экспортируется ли языковая информация в HTML, MHTML или EPUB. Значение по умолчанию:`ЛОЖЬ` . |
| [ExportListLabels](../../aspose.words.saving/htmlsaveoptions/exportlistlabels/) { get; set; } | Управляет выводом меток списков в HTML, MHTML или EPUB. Значение по умолчанию:Auto . |
| [ExportOriginalUrlForLinkedImages](../../aspose.words.saving/htmlsaveoptions/exportoriginalurlforlinkedimages/) { get; set; } | Указывает, следует ли использовать исходный URL-адрес в качестве URL-адреса связанных изображений. Значение по умолчанию:`ЛОЖЬ` . |
| [ExportPageMargins](../../aspose.words.saving/htmlsaveoptions/exportpagemargins/) { get; set; } | Указывает, экспортируются ли поля страницы в HTML, MHTML или EPUB. Значение по умолчанию:`ЛОЖЬ` . |
| [ExportPageSetup](../../aspose.words.saving/htmlsaveoptions/exportpagesetup/) { get; set; } | Указывает, экспортируются ли настройки страницы в HTML, MHTML или EPUB. Значение по умолчанию:`ЛОЖЬ` . |
| [ExportRelativeFontSize](../../aspose.words.saving/htmlsaveoptions/exportrelativefontsize/) { get; set; } | Указывает, следует ли выводить размеры шрифта в относительных единицах при сохранении в HTML, MHTML или EPUB. Значение по умолчанию:`ЛОЖЬ` . |
| [ExportRoundtripInformation](../../aspose.words.saving/htmlsaveoptions/exportroundtripinformation/) { get; set; } | Указывает, следует ли записывать информацию о цикле передачи при сохранении в формате HTML, MHTML или EPUB. Значение по умолчанию:`истинный` для HTML и`ЛОЖЬ` для MHTML и EPUB. |
| [ExportShapesAsSvg](../../aspose.words.saving/htmlsaveoptions/exportshapesassvg/) { get; set; } | Управляет тем,[`Shape`](../../aspose.words.drawing/shape/)узлы преобразуются в изображения SVG при сохранении в HTML, MHTML, EPUB или AZW3. Значение по умолчанию:`ЛОЖЬ` . |
| [ExportTextInputFormFieldAsText](../../aspose.words.saving/htmlsaveoptions/exporttextinputformfieldastext/) { get; set; } | Управляет сохранением полей формы ввода текста в HTML или MHTML. Значение по умолчанию:`ЛОЖЬ` . |
| [ExportTocPageNumbers](../../aspose.words.saving/htmlsaveoptions/exporttocpagenumbers/) { get; set; } | Указывает, следует ли записывать номера страниц в оглавление при сохранении HTML, MHTML и EPUB. Значение по умолчанию:`ЛОЖЬ` . |
| [ExportXhtmlTransitional](../../aspose.words.saving/htmlsaveoptions/exportxhtmltransitional/) { get; set; } | Указывает, следует ли записывать декларацию DOCTYPE при сохранении в HTML или MHTML. Когда`истинный` , записывает объявление DOCTYPE в документ перед корневым элементом. Значение по умолчанию:`ЛОЖЬ`. При сохранении в формате EPUB или HTML5 (Html5 ) всегда записывается декларация DOCTYPE . |
| [FontResourcesSubsettingSizeThreshold](../../aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold/) { get; set; } | Управляет тем, какие ресурсы шрифта требуют поднабора при сохранении в HTML, MHTML или EPUB. Значение по умолчанию:`0` . |
| [FontSavingCallback](../../aspose.words.saving/htmlsaveoptions/fontsavingcallback/) { get; set; } | Позволяет контролировать сохранение шрифтов при сохранении документа в формате HTML, MHTML или EPUB. |
| [FontsFolder](../../aspose.words.saving/htmlsaveoptions/fontsfolder/) { get; set; } | Указывает физическую папку, в которой сохраняются шрифты при экспорте документа в HTML. По умолчанию — пустая строка. |
| [FontsFolderAlias](../../aspose.words.saving/htmlsaveoptions/fontsfolderalias/) { get; set; } | Указывает имя папки, используемой для создания URI шрифтов, записанных в HTML-документ. По умолчанию — пустая строка. |
| [HtmlVersion](../../aspose.words.saving/htmlsaveoptions/htmlversion/) { get; set; } | Указывает версию стандарта HTML, которую следует использовать при сохранении документа в формате HTML или MHTML. Значение по умолчанию:Xhtml . |
| [ImageResolution](../../aspose.words.saving/htmlsaveoptions/imageresolution/) { get; set; } | Указывает выходное разрешение для изображений при экспорте в HTML, MHTML или EPUB. Значение по умолчанию:`96 точек на дюйм` . |
| [ImageSavingCallback](../../aspose.words.saving/htmlsaveoptions/imagesavingcallback/) { get; set; } | Позволяет контролировать способ сохранения изображений при сохранении документа в формате HTML, MHTML или EPUB. |
| [ImagesFolder](../../aspose.words.saving/htmlsaveoptions/imagesfolder/) { get; set; } | Указывает физическую папку, в которой сохраняются изображения при экспорте документа в формат HTML. По умолчанию — пустая строка. |
| [ImagesFolderAlias](../../aspose.words.saving/htmlsaveoptions/imagesfolderalias/) { get; set; } | Указывает имя папки, используемой для создания URI изображений, записанных в HTML-документ. По умолчанию — пустая строка. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Возвращает или задает значение, определяющее способ визуализации объектов рукописного ввода (InkML). |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Возвращает или задает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойства:`ЛОЖЬ` . |
| [MetafileFormat](../../aspose.words.saving/htmlsaveoptions/metafileformat/) { get; set; } | Указывает, в каком формате сохраняются метафайлы при экспорте в HTML, MHTML или EPUB. Значение по умолчанию:Png , что означает, что метафайлы преобразуются в растровые изображения PNG. |
| [NavigationMapLevel](../../aspose.words.saving/htmlsaveoptions/navigationmaplevel/) { get; set; } | Указывает максимальный уровень заголовков, заполняемых на навигационной карте при экспорте в форматы EPUB, MOBI или AZW3 . Значение по умолчанию:`3` . |
| [OfficeMathOutputMode](../../aspose.words.saving/htmlsaveoptions/officemathoutputmode/) { get; set; } | Управляет экспортом объектов OfficeMath в HTML, MHTML или EPUB. Значение по умолчанию:Image . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Когда`истинный` , красивые форматы вывода, где это применимо. Значение по умолчанию:`ЛОЖЬ` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Вызывается во время сохранения документа и принимает данные о ходе сохранения. |
| [RemoveJavaScriptFromLinks](../../aspose.words.saving/htmlsaveoptions/removejavascriptfromlinks/) { get; set; } | Указывает, будет ли JavaScript удален из ссылок. Значение по умолчанию:`ЛОЖЬ` . |
| [ReplaceBackslashWithYenSign](../../aspose.words.saving/htmlsaveoptions/replacebackslashwithyensign/) { get; set; } | Указывает, следует ли заменять символы обратной косой черты на знаки йены. Значение по умолчанию:`ЛОЖЬ` . |
| [ResolveFontNames](../../aspose.words.saving/htmlsaveoptions/resolvefontnames/) { get; set; } | Указывает, разрешаются ли и заменяются ли имена семейств шрифтов, используемые в документе, в соответствии с [`FontSettings`](../../aspose.words/document/fontsettings/) при записи в форматы на основе HTML. |
| [ResourceFolder](../../aspose.words.saving/htmlsaveoptions/resourcefolder/) { get; set; } | Указывает физическую папку, в которой сохраняются все ресурсы, такие как изображения, шрифты и внешний CSS, когда document экспортируется в HTML. По умолчанию — пустая строка. |
| [ResourceFolderAlias](../../aspose.words.saving/htmlsaveoptions/resourcefolderalias/) { get; set; } | Указывает имя папки, используемой для построения URI всех ресурсов, записанных в HTML-документ. По умолчанию — пустая строка. |
| override [SaveFormat](../../aspose.words.saving/htmlsaveoptions/saveformat/) { get; set; } | Указывает формат, в котором будет сохранен документ, если используется этот объект параметров сохранения. Может бытьHtml ,Mhtml ,Epub , Azw3 илиMobi . |
| [ScaleImageToShapeSize](../../aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize/) { get; set; } | Указывает, масштабируются ли изображения Aspose.Words до размера ограничивающей фигуры при экспорте в HTML, MHTML или EPUB. Значение по умолчанию:`истинный` . |
| [TableWidthOutputMode](../../aspose.words.saving/htmlsaveoptions/tablewidthoutputmode/) { get; set; } | Управляет экспортом ширины таблицы, строк и ячеек в HTML, MHTML или EPUB. Значение по умолчанию:All . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Указывает папку для временных файлов, используемых при сохранении в файл DOC или DOCX. По умолчанию это свойство`нулевой` и временные файлы не используются. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Определяет, будут ли изменяться атрибуты шрифта в соответствии с используемым кодом символа. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Возвращает или задает значение, определяющее, является ли[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) свойство обновляется перед сохранением. Значение по умолчанию:`ЛОЖЬ` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Возвращает или задает значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы. Значение по умолчанию для этого свойства:`истинный` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Возвращает или задает значение, определяющее, является ли[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) свойство обновляется перед сохранением. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Возвращает или задает значение, определяющее, является ли[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) свойство обновляется перед сохранением. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Возвращает или задает значение, определяющее, следует ли использовать сглаживание при рендеринге. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Возвращает или задает значение, определяющее, следует ли использовать высококачественные (т. е. медленные) алгоритмы рендеринга. |

## Примеры

Показывает, как указать папку для хранения связанных изображений после сохранения в формате .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// Установите параметр для экспорта полей формы как обычного текста вместо элементов ввода HTML.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

Показывает, как использовать определенную кодировку при сохранении документа в формате .epub.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Используйте объект SaveOptions, чтобы указать кодировку документа, который мы будем сохранять.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// По умолчанию выходной документ .epub будет иметь все свое содержимое в одной части HTML.
// Критерий разделения позволяет нам сегментировать документ на несколько частей HTML.
// Мы установим критерии для разделения документа на заголовочные абзацы.
// Это полезно для читателей, которые не могут читать HTML-файлы, размер которых больше определенного значения.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Указываем, что мы хотим экспортировать свойства документа.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

Показывает, как разделить документ на части и сохранить их.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // Создаем объект "HtmlFixedSaveOptions", который можно передать методу "Save" документа
    // чтобы изменить способ преобразования документа в HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Если мы сохраним документ обычным образом, будет один выходной HTML
    // документ со всем содержимым исходного документа.
    // Установите свойство "DocumentSplitCriteria" в "DocumentSplitCriteria.SectionBreak" для
    // сохраняем наш документ в несколько HTML-файлов: по одному для каждого раздела.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // Назначьте пользовательский обратный вызов свойству "DocumentPartSavingCallback", чтобы изменить логику сохранения части документа.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // Если мы преобразуем документ, содержащий изображения, в html, мы получим один html-файл, который ссылается на несколько изображений.
    // Каждое изображение будет иметь форму файла в локальной файловой системе.
    // Также имеется обратный вызов, который позволяет настраивать имя и местоположение каждого изображения в файловой системе.
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
        // Мы можем получить доступ ко всему исходному документу через свойство «Документ».
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

        // Ниже приведены два способа указания того, где Aspose.Words будет сохранять каждую часть документа.
        // 1 - Задайте имя файла для выходного файла детали:
        args.DocumentPartFileName = partFileName;

        // 2 - Создать пользовательский поток для выходного файла детали:
        args.DocumentPartStream = new FileStream(ArtifactsDir + partFileName, FileMode.Create);

        Assert.True(args.DocumentPartStream.CanWrite);
        Assert.False(args.KeepDocumentPartStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
    private readonly DocumentSplitCriteria mDocumentSplitCriteria;
}

/// <summary>
/// Задает пользовательские имена файлов изображений, создаваемых при преобразовании HTML.
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

        // Ниже приведены два способа указания того, где Aspose.Words будет сохранять каждую часть документа.
        // 1 — Задайте имя файла для выходного изображения:
        args.ImageFileName = imageFileName;

        // 2 — Создать пользовательский поток для выходного файла изображения:
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

* class [SaveOptions](../saveoptions/)
* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
