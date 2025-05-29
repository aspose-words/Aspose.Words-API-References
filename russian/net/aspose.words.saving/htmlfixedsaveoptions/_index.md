---
title: HtmlFixedSaveOptions Class
linktitle: HtmlFixedSaveOptions
articleTitle: HtmlFixedSaveOptions
second_title: Aspose.Words для .NET
description: Откройте для себя Aspose.Words.Saving.HtmlFixedSaveOptions, чтобы улучшить ваш опыт сохранения документов. Настройте параметры для оптимального вывода в формате HtmlFixed.
type: docs
weight: 5830
url: /ru/net/aspose.words.saving/htmlfixedsaveoptions/
---
## HtmlFixedSaveOptions class

Может использоваться для указания дополнительных параметров при сохранении документа вHtmlFixed формат.

Чтобы узнать больше, посетите[Укажите параметры сохранения](https://docs.aspose.com/words/net/specify-save-options/) документальная статья.

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
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Возвращает или задает логическое значение, указывающее, разрешать ли встраивание шрифтов с контурами PostScript при встраивании шрифтов TrueType в документ при его сохранении. Значение по умолчанию:`ЛОЖЬ` . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | Возвращает или задает значение, определяющее способ отображения цветов. |
| [CssClassNamesPrefix](../../aspose.words.saving/htmlfixedsaveoptions/cssclassnamesprefix/) { get; set; } | Указывает префикс, который добавляется ко всем именам классов в файле style.css. Значение по умолчанию:`"ой"` . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Возвращает или задает пользовательский локальный часовой пояс, используемый для полей даты/времени. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Возвращает или задает путь к шаблону по умолчанию (включая имя файла). Значение по умолчанию для этого свойства:**пустая строка** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Возвращает или задает значение, определяющее способ визуализации 3D-эффектов. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Возвращает или задает значение, определяющее способ визуализации эффектов DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Возвращает или задает значение, определяющее способ визуализации фигур DrawingML. |
| [Encoding](../../aspose.words.saving/htmlfixedsaveoptions/encoding/) { get; set; } | Указывает кодировку, используемую при экспорте в HTML. Значение по умолчанию:`новая кодировка UTF8(истина)` (UTF-8 с BOM). |
| [ExportEmbeddedCss](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedcss/) { get; set; } | Указывает, следует ли встраивать CSS (каскадную таблицу стилей) в HTML-документ. |
| [ExportEmbeddedFonts](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedfonts/) { get; set; } | Указывает, следует ли встраивать шрифты в HTML-документ в формате Base64. Обратите внимание, что установка этого флага может значительно увеличить размер выходного HTML-файла. |
| [ExportEmbeddedImages](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedimages/) { get; set; } | Указывает, следует ли встраивать изображения в HTML-документ в формате Base64. Обратите внимание, что установка этого флага может значительно увеличить размер выходного HTML-файла. |
| [ExportEmbeddedSvg](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedsvg/) { get; set; } | Указывает, следует ли встраивать ресурсы SVG в документ HTML. Значение по умолчанию:`истинный` . |
| [ExportFormFields](../../aspose.words.saving/htmlfixedsaveoptions/exportformfields/) { get; set; } | Возвращает или задает указание того, экспортируются ли поля формы как интерактивные элементы (как тег «input»), а не преобразуются в текст или графику. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Когда`истинный` , приводит к внедрению имени и версии Aspose.Words в создаваемые файлы. Значение по умолчанию:`истинный` . |
| [FontFormat](../../aspose.words.saving/htmlfixedsaveoptions/fontformat/) { get; set; } | Получает или устанавливает[`ExportFontFormat`](../exportfontformat/) используется для экспорта шрифтов. Значение по умолчанию:Woff . |
| [IdPrefix](../../aspose.words.saving/htmlfixedsaveoptions/idprefix/) { get; set; } | Указывает префикс, который добавляется ко всем сгенерированным идентификаторам элементов в выходном документе. Значение по умолчанию — null, и префикс не добавляется. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Возвращает или задает значение, определяющее способ визуализации объектов рукописного ввода (InkML). |
| [JpegQuality](../../aspose.words.saving/fixedpagesaveoptions/jpegquality/) { get; set; } | Возвращает или задает значение, определяющее качество изображений JPEG внутри документа HTML. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Возвращает или задает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойства:`ЛОЖЬ` . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/) { get; set; } | Позволяет указать параметры рендеринга метафайла. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | Получает или устанавливает[`NumeralFormat`](../numeralformat/) используется для отображения цифр. По умолчанию используются европейские цифры. |
| override [OptimizeOutput](../../aspose.words.saving/htmlfixedsaveoptions/optimizeoutput/) { get; set; } | Флаг указывает, требуется ли оптимизировать вывод. Если этот флаг установлен, избыточные вложенные холсты и пустые холсты удаляются, также объединяются соседние глифы с одинаковым форматированием. Примечание: Точность отображения содержимого может быть затронута, если это свойство установлено в`истинный` . По умолчанию`истинный` . |
| [PageHorizontalAlignment](../../aspose.words.saving/htmlfixedsaveoptions/pagehorizontalalignment/) { get; set; } | Задает горизонтальное выравнивание страниц в документе HTML. Значение по умолчанию:Center . |
| [PageMargins](../../aspose.words.saving/htmlfixedsaveoptions/pagemargins/) { get; set; } | Задает поля вокруг страниц в документе HTML. Значение полей измеряется в пунктах и должно быть равно или больше 0. Значение по умолчанию — 10 пунктов. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Позволяет контролировать, как сохраняются отдельные страницы при экспорте документа в формат фиксированной страницы. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset/) { get; set; } | Получает или задает страницы для отображения. По умолчанию — все страницы в документе. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Когда`истинный` , красивые форматы вывода, где это применимо. Значение по умолчанию:`ЛОЖЬ` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Вызывается во время сохранения документа и принимает данные о ходе сохранения. |
| [RemoveJavaScriptFromLinks](../../aspose.words.saving/htmlfixedsaveoptions/removejavascriptfromlinks/) { get; set; } | Указывает, будет ли JavaScript удален из ссылок. Значение по умолчанию:`ЛОЖЬ` . |
| [ResourceSavingCallback](../../aspose.words.saving/htmlfixedsaveoptions/resourcesavingcallback/) { get; set; } | Позволяет контролировать, как сохраняются ресурсы (изображения, шрифты и css) при экспорте документа в формат HTML с фиксированной страницей. |
| [ResourcesFolder](../../aspose.words.saving/htmlfixedsaveoptions/resourcesfolder/) { get; set; } | Указывает физическую папку, в которой сохраняются ресурсы (изображения, шрифты, css) при экспорте документа в формат HTML. Значение по умолчанию:`нулевой` . |
| [ResourcesFolderAlias](../../aspose.words.saving/htmlfixedsaveoptions/resourcesfolderalias/) { get; set; } | Указывает имя папки, используемой для создания URI изображений, записанных в HTML-документ. Значение по умолчанию:`нулевой` . |
| [SaveFontFaceCssSeparately](../../aspose.words.saving/htmlfixedsaveoptions/savefontfacecssseparately/) { get; set; } | Флаг указывает, следует ли помещать правила CSS "@font-face" в отдельный файл "fontFaces.css" при сохранении документа с внешней таблицей стилей (то есть, когда[`ExportEmbeddedCss`](./exportembeddedcss/) это`ЛОЖЬ` ). Значение по умолчанию:`ЛОЖЬ` , все правила CSS записаны в один файл "styles.css". |
| override [SaveFormat](../../aspose.words.saving/htmlfixedsaveoptions/saveformat/) { get; set; } | Указывает формат, в котором будет сохранен документ, если используется этот объект параметров сохранения. Может быть толькоHtmlFixed . |
| [ShowPageBorder](../../aspose.words.saving/htmlfixedsaveoptions/showpageborder/) { get; set; } | Указывает, следует ли отображать границу вокруг страниц. Значение по умолчанию:`истинный` . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Указывает папку для временных файлов, используемых при сохранении в файл DOC или DOCX. По умолчанию это свойство`нулевой` и временные файлы не используются. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Определяет, будут ли изменяться атрибуты шрифта в соответствии с используемым кодом символа. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Возвращает или задает значение, определяющее, является ли[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) свойство обновляется перед сохранением. Значение по умолчанию:`ЛОЖЬ` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Возвращает или задает значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы. Значение по умолчанию для этого свойства:`истинный` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Возвращает или задает значение, определяющее, является ли[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) свойство обновляется перед сохранением. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Возвращает или задает значение, определяющее, является ли[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) свойство обновляется перед сохранением. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Возвращает или задает значение, определяющее, следует ли использовать сглаживание при рендеринге. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Возвращает или задает значение, определяющее, следует ли использовать высококачественные (т. е. медленные) алгоритмы рендеринга. |
| [UseTargetMachineFonts](../../aspose.words.saving/htmlfixedsaveoptions/usetargetmachinefonts/) { get; set; } | Флаг указывает, должны ли использоваться шрифты с целевой машины для отображения документа. Если этот флаг установлен в`истинный` ,[`FontFormat`](./fontformat/) и[`ExportEmbeddedFonts`](./exportembeddedfonts/) свойства не имеют эффекта, также[`ResourceSavingCallback`](./resourcesavingcallback/) не запускается для шрифтов. По умолчанию`ЛОЖЬ` . |

## Методы

| Имя | Описание |
| --- | --- |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(*object*) | Определяет, равен ли указанный объект по значению текущему объекту. |

## Примеры

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

    // Папка, указанная ResourcesFolderAlias, будет содержать ресурсы вместо ResourcesFolder.
    // Мы должны убедиться, что папка существует, прежде чем потоки смогут поместить в нее свои ресурсы.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

    Console.WriteLine(callback.GetText());

    string[] resourceFiles = Directory.GetFiles(ArtifactsDir + "HtmlFixedResourceFolderAlias");

    Assert.False(Directory.Exists(ArtifactsDir + "HtmlFixedResourceFolder"));
    Assert.AreEqual(6, resourceFiles.Count(f => f.EndsWith(".jpeg") || f.EndsWith(".png") || f.EndsWith(".css")));
}

/// <summary>
/// Подсчитывает и выводит URI ресурсов, содержащихся в, по мере их преобразования в фиксированный HTML.
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
                // По умолчанию «ResourceFileUri» использует системную папку для шрифтов.
                // Чтобы избежать проблем на других платформах, необходимо явно указать путь к шрифтам.
                args.ResourceFileUri = ArtifactsDir + Path.DirectorySeparatorChar + args.ResourceFileName;
                break;
            }
        }

        mText.AppendLine("\t" + args.ResourceFileUri);

        // Если мы указали папку в свойстве "ResourcesFolderAlias",
        // нам также потребуется перенаправить каждый поток, чтобы поместить его ресурс в эту папку.
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
