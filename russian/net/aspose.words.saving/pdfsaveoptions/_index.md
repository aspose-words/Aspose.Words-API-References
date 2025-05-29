---
title: PdfSaveOptions Class
linktitle: PdfSaveOptions
articleTitle: PdfSaveOptions
second_title: Aspose.Words для .NET
description: Откройте для себя Aspose.Words.PdfSaveOptions, чтобы улучшить ваш опыт сохранения документов. Настройте параметры для оптимального качества и производительности вывода PDF.
type: docs
weight: 6320
url: /ru/net/aspose.words.saving/pdfsaveoptions/
---
## PdfSaveOptions class

Может использоваться для указания дополнительных параметров при сохранении документа вPdf формат.

Чтобы узнать больше, посетите[Укажите параметры сохранения](https://docs.aspose.com/words/net/specify-save-options/) документальная статья.

```csharp
public class PdfSaveOptions : FixedPageSaveOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [PdfSaveOptions](pdfsaveoptions/)() | Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа в Pdf формат. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [AdditionalTextPositioning](../../aspose.words.saving/pdfsaveoptions/additionaltextpositioning/) { get; set; } | Флаг, указывающий, следует ли записывать дополнительные операторы позиционирования текста или нет. |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Возвращает или задает логическое значение, указывающее, разрешать ли встраивание шрифтов с контурами PostScript при встраивании шрифтов TrueType в документ при его сохранении. Значение по умолчанию:`ЛОЖЬ` . |
| [AttachmentsEmbeddingMode](../../aspose.words.saving/pdfsaveoptions/attachmentsembeddingmode/) { get; set; } | Возвращает или задает значение, определяющее, как вложения внедряются в документ PDF. |
| [CacheBackgroundGraphics](../../aspose.words.saving/pdfsaveoptions/cachebackgroundgraphics/) { get; set; } | Возвращает или задает значение, определяющее, следует ли кэшировать графику, размещенную в фоне документа. |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | Возвращает или задает значение, определяющее способ отображения цветов. |
| [Compliance](../../aspose.words.saving/pdfsaveoptions/compliance/) { get; set; } | Указывает уровень соответствия стандартам PDF для выходных документов. |
| [CreateNoteHyperlinks](../../aspose.words.saving/pdfsaveoptions/createnotehyperlinks/) { get; set; } | Указывает, следует ли преобразовывать ссылки на сноски/концевые сноски в основном тексте статьи в активные гиперссылки. При щелчке по гиперссылке будет открыта соответствующая сноска/концевая сноска. Значение по умолчанию:`ЛОЖЬ` . |
| [CustomPropertiesExport](../../aspose.words.saving/pdfsaveoptions/custompropertiesexport/) { get; set; } | Возвращает или задает значение, определяющее способ[`CustomDocumentProperties`](../../aspose.words/document/customdocumentproperties/) экспортируются в файл PDF. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Возвращает или задает пользовательский локальный часовой пояс, используемый для полей даты/времени. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Возвращает или задает путь к шаблону по умолчанию (включая имя файла). Значение по умолчанию для этого свойства:**пустая строка** (Empty ). |
| [DigitalSignatureDetails](../../aspose.words.saving/pdfsaveoptions/digitalsignaturedetails/) { get; set; } | Получает или задает данные для подписания выходного PDF-документа. |
| [DisplayDocTitle](../../aspose.words.saving/pdfsaveoptions/displaydoctitle/) { get; set; } | Флаг, указывающий, должно ли в строке заголовка окна отображаться название документа, взятое из записи «Название» словаря информации о документе. |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Возвращает или задает значение, определяющее способ визуализации 3D-эффектов. |
| override [DmlEffectsRenderingMode](../../aspose.words.saving/pdfsaveoptions/dmleffectsrenderingmode/) { get; set; } | Возвращает или задает значение, определяющее способ визуализации эффектов DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Возвращает или задает значение, определяющее способ визуализации фигур DrawingML. |
| [DownsampleOptions](../../aspose.words.saving/pdfsaveoptions/downsampleoptions/) { get; set; } | Позволяет указать параметры понижения разрешения. |
| [EmbedFullFonts](../../aspose.words.saving/pdfsaveoptions/embedfullfonts/) { get; set; } | Управляет тем, как шрифты внедряются в результирующие PDF-документы. |
| [EncryptionDetails](../../aspose.words.saving/pdfsaveoptions/encryptiondetails/) { get; set; } | Возвращает или задает параметры шифрования выходного PDF-документа. |
| [ExportDocumentStructure](../../aspose.words.saving/pdfsaveoptions/exportdocumentstructure/) { get; set; } | Возвращает или задает значение, определяющее, следует ли экспортировать структуру документа. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Когда`истинный` , приводит к внедрению имени и версии Aspose.Words в создаваемые файлы. Значение по умолчанию:`истинный` . |
| [ExportLanguageToSpanTag](../../aspose.words.saving/pdfsaveoptions/exportlanguagetospantag/) { get; set; } | Возвращает или задает значение, определяющее, следует ли создавать тег «Span» в структуре документа для экспорта языка текста. |
| [ExportParagraphGraphicsToArtifact](../../aspose.words.saving/pdfsaveoptions/exportparagraphgraphicstoartifact/) { get; set; } | Возвращает или задает значение, определяющее, следует ли помечать графический элемент абзаца как артефакт. |
| [FontEmbeddingMode](../../aspose.words.saving/pdfsaveoptions/fontembeddingmode/) { get; set; } | Указывает режим внедрения шрифта. |
| [HeaderFooterBookmarksExportMode](../../aspose.words.saving/pdfsaveoptions/headerfooterbookmarksexportmode/) { get; set; } | Определяет, как экспортируются закладки в верхних/нижних колонтитулах. |
| [ImageColorSpaceExportMode](../../aspose.words.saving/pdfsaveoptions/imagecolorspaceexportmode/) { get; set; } | Указывает, как будет выбрано цветовое пространство для изображений в документе PDF. |
| [ImageCompression](../../aspose.words.saving/pdfsaveoptions/imagecompression/) { get; set; } | Указывает тип сжатия, который будет использоваться для всех изображений в документе. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Возвращает или задает значение, определяющее способ визуализации объектов рукописного ввода (InkML). |
| [InterpolateImages](../../aspose.words.saving/pdfsaveoptions/interpolateimages/) { get; set; } | Флаг, указывающий, должна ли выполняться интерполяция изображения соответствующим считывателем. Когда`ЛОЖЬ` указан, флаг не записывается в выходной документ и вместо этого используется поведение читателя по умолчанию. |
| [JpegQuality](../../aspose.words.saving/pdfsaveoptions/jpegquality/) { get; set; } | Возвращает или задает значение, определяющее качество изображений JPEG в документе PDF. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Возвращает или задает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойства:`ЛОЖЬ` . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/) { get; set; } | Позволяет указать параметры рендеринга метафайла. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | Получает или устанавливает[`NumeralFormat`](../numeralformat/) используется для отображения цифр. По умолчанию используются европейские цифры. |
| [OpenHyperlinksInNewWindow](../../aspose.words.saving/pdfsaveoptions/openhyperlinksinnewwindow/) { get; set; } | Возвращает или задает значение, определяющее, будут ли гиперссылки в выходном документе PDF принудительно открываться в новом окне (или вкладке) браузера. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput/) { get; set; } | Флаг указывает, требуется ли оптимизировать вывод. Если этот флаг установлен, избыточные вложенные холсты и пустые холсты удаляются, также объединяются соседние глифы с одинаковым форматированием. Примечание: Точность отображения содержимого может быть затронута, если это свойство установлено в`истинный` . По умолчанию`ЛОЖЬ` . |
| [OutlineOptions](../../aspose.words.saving/pdfsaveoptions/outlineoptions/) { get; } | Позволяет указать параметры контура. |
| [PageLayout](../../aspose.words.saving/pdfsaveoptions/pagelayout/) { get; set; } | Указывает макет страницы, который будет использоваться при открытии документа в программе для чтения PDF-файлов. |
| [PageMode](../../aspose.words.saving/pdfsaveoptions/pagemode/) { get; set; } | Указывает, как должен отображаться PDF-документ при открытии в программе для чтения PDF-файлов. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Позволяет контролировать, как сохраняются отдельные страницы при экспорте документа в формат фиксированной страницы. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset/) { get; set; } | Получает или задает страницы для отображения. По умолчанию — все страницы в документе. |
| [PreblendImages](../../aspose.words.saving/pdfsaveoptions/preblendimages/) { get; set; } | Возвращает или задает значение, определяющее, следует ли предварительно смешивать прозрачные изображения с черным фоновым цветом. |
| [PreserveFormFields](../../aspose.words.saving/pdfsaveoptions/preserveformfields/) { get; set; } | Указывает, следует ли сохранять поля формы Microsoft Word как поля формы в PDF или преобразовывать их в текст. Значение по умолчанию:`ЛОЖЬ` . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Когда`истинный` , красивые форматы вывода, где это применимо. Значение по умолчанию:`ЛОЖЬ` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Вызывается во время сохранения документа и принимает данные о ходе сохранения. |
| [RenderChoiceFormFieldBorder](../../aspose.words.saving/pdfsaveoptions/renderchoiceformfieldborder/) { get; set; } | Указывает, отображать ли границу поля формы выбора PDF. |
| override [SaveFormat](../../aspose.words.saving/pdfsaveoptions/saveformat/) { get; set; } | Указывает формат, в котором будет сохранен документ, если используется этот объект параметров сохранения. Может быть толькоPdf . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Указывает папку для временных файлов, используемых при сохранении в файл DOC или DOCX. По умолчанию это свойство`нулевой` и временные файлы не используются. |
| [TextCompression](../../aspose.words.saving/pdfsaveoptions/textcompression/) { get; set; } | Указывает тип сжатия, который будет использоваться для всего текстового содержимого документа. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Определяет, будут ли изменяться атрибуты шрифта в соответствии с используемым кодом символа. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Возвращает или задает значение, определяющее, является ли[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) свойство обновляется перед сохранением. Значение по умолчанию:`ЛОЖЬ` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Возвращает или задает значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы. Значение по умолчанию для этого свойства:`истинный` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Возвращает или задает значение, определяющее, является ли[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) свойство обновляется перед сохранением. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Возвращает или задает значение, определяющее, является ли[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) свойство обновляется перед сохранением. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Возвращает или задает значение, определяющее, следует ли использовать сглаживание при рендеринге. |
| [UseBookFoldPrintingSettings](../../aspose.words.saving/pdfsaveoptions/usebookfoldprintingsettings/) { get; set; } | Возвращает или задает логическое значение, указывающее, следует ли сохранять документ с использованием макета печати буклета, , если он указан через[`MultiplePages`](../../aspose.words/pagesetup/multiplepages/) . |
| [UseCoreFonts](../../aspose.words.saving/pdfsaveoptions/usecorefonts/) { get; set; } | Возвращает или задает значение, определяющее, следует ли заменять шрифты TrueType Arial, Times New Roman, Courier New и Symbol основными шрифтами PDF Type 1. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Возвращает или задает значение, определяющее, следует ли использовать высококачественные (т. е. медленные) алгоритмы рендеринга. |
| [UseSdtTagAsFormFieldName](../../aspose.words.saving/pdfsaveoptions/usesdttagasformfieldname/) { get; set; } | Указывает, следует ли использовать тег элемента управления SDT или свойство Id в качестве имени поля формы в PDF. |
| [ZoomBehavior](../../aspose.words.saving/pdfsaveoptions/zoombehavior/) { get; set; } | Возвращает или задает значение, определяющее, какой тип масштабирования следует применять при открытии документа с помощью средства просмотра PDF-файлов. |
| [ZoomFactor](../../aspose.words.saving/pdfsaveoptions/zoomfactor/) { get; set; } | Возвращает или задает значение, определяющее коэффициент масштабирования (в процентах) для документа. |

## Методы

| Имя | Описание |
| --- | --- |
| [Clone](../../aspose.words.saving/pdfsaveoptions/clone/)() | Создает глубокую копию этого объекта. |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(*object*) | Определяет, равен ли указанный объект по значению текущему объекту. |

## Примеры

Показывает, как изменить цвет изображения с сохранением свойств параметров.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
// Установите свойство «ColorMode» на «Grayscale», чтобы отрисовать все изображения в документе в черно-белом цвете.
// При использовании этой настройки размер выходного документа может быть больше.
// Установите свойство «ColorMode» на «Normal», чтобы отображать все изображения в цвете.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { ColorMode = colorMode };

doc.Save(ArtifactsDir + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

Показывает, как применять сжатие текста при сохранении документа в формате PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 100; i++)
    builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                    "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Установите свойство "TextCompression" на "PdfTextCompression.None", чтобы не применять никаких
// сжатие в текст при сохранении документа в формате PDF.
// Установите свойство "TextCompression" на "PdfTextCompression.Flate", чтобы применить сжатие ZIP
// в текст при сохранении документа в PDF. Чем больше документ, тем больше будет влияние.
options.TextCompression = pdfTextCompression;

doc.Save(ArtifactsDir + "PdfSaveOptions.TextCompression.pdf", options);
```

Показывает, как преобразовать весь документ в PDF с тремя уровнями в структуре документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте заголовки уровней с 1 по 5.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;

builder.Writeln("Heading 1.2.2.1");
builder.Writeln("Heading 1.2.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.2.2.2.1");
builder.Writeln("Heading 1.2.2.2.2");

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Выходной PDF-документ будет содержать структуру, представляющую собой оглавление, в котором перечислены заголовки в тексте документа.
// Нажатие на запись в этой схеме перенесет нас к местоположению соответствующего заголовка.
// Установите свойство "HeadingsOutlineLevels" на "4", чтобы исключить из структуры все заголовки, уровни которых выше 4.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// Если запись структуры имеет последующие записи более высокого уровня между собой и следующей записью того же или более низкого уровня,
// слева от записи появится стрелка. Эта запись является «владельцем» нескольких таких «подзаписей».
// В нашем документе записи структуры из 5-го уровня заголовка являются подзаписями второй записи структуры 4-го уровня,
// записи 4-го и 5-го уровня заголовка являются подзаголовками второй записи 3-го уровня и т. д.
// В схеме мы можем щелкнуть стрелку записи «владелец», чтобы свернуть/развернуть все ее подзаписи.
// Установите свойство "ExpandedOutlineLevels" на "2", чтобы автоматически развернуть все заголовки уровня 2 и более низких записей структуры
// и сворачиваем все записи уровня 3 и выше при открытии документа.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### Смотрите также

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
