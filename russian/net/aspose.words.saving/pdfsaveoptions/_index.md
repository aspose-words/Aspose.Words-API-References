---
title: PdfSaveOptions
second_title: Справочник по API Aspose.Words для .NET
description: Может использоваться для указания дополнительных параметров при сохранении документа вPdf формат.
type: docs
weight: 5240
url: /ru/net/aspose.words.saving/pdfsaveoptions/
---
## PdfSaveOptions class

Может использоваться для указания дополнительных параметров при сохранении документа вPdf формат.

```csharp
public class PdfSaveOptions : FixedPageSaveOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [PdfSaveOptions](pdfsaveoptions)() | Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа в папке .Pdf формат. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [AdditionalTextPositioning](../../aspose.words.saving/pdfsaveoptions/additionaltextpositioning) { get; set; } | Флаг, указывающий, следует ли писать дополнительные операторы позиционирования текста или нет. |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts) { get; set; } | Возвращает или задает логическое значение, указывающее, разрешать ли встраивание шрифтов с помощью PostScript layouts при встраивании шрифтов TrueType в документ после его сохранения. Значение по умолчанию: **ЛОЖЬ** . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode) { get; set; } | Получает или задает значение, определяющее способ отображения цветов. |
| [Compliance](../../aspose.words.saving/pdfsaveoptions/compliance) { get; set; } | Указывает уровень соответствия стандартам PDF для выходных документов. |
| [CreateNoteHyperlinks](../../aspose.words.saving/pdfsaveoptions/createnotehyperlinks) { get; set; } | Указывает, следует ли преобразовывать ссылки на сноску/концевую сноску в основном текстовом материале в активные гиперссылки. При щелчке гиперссылка приведет к соответствующей сноске/концевой сноске. Значение по умолчанию:`ЛОЖЬ` . |
| [CustomPropertiesExport](../../aspose.words.saving/pdfsaveoptions/custompropertiesexport) { get; set; } | Получает или задает значение, определяющее способ[`CustomDocumentProperties`](../../aspose.words/document/customdocumentproperties) экспортируются в файл PDF. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo) { get; set; } | Получает или задает пользовательский местный часовой пояс, используемый для полей даты/времени. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate) { get; set; } | Получает или задает путь к шаблону по умолчанию (включая имя файла). Значение по умолчанию для этого свойства: **пустой строки** (Empty ). |
| [DigitalSignatureDetails](../../aspose.words.saving/pdfsaveoptions/digitalsignaturedetails) { get; set; } | Получает или задает сведения для подписания выходного PDF-документа. |
| [DisplayDocTitle](../../aspose.words.saving/pdfsaveoptions/displaydoctitle) { get; set; } | Флаг, указывающий, должен ли заголовок окна отображать заголовок документа, взятый из элемента Title словаря информации о документе. |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode) { get; set; } | Получает или задает значение, определяющее способ визуализации 3D-эффектов. |
| override [DmlEffectsRenderingMode](../../aspose.words.saving/pdfsaveoptions/dmleffectsrenderingmode) { get; set; } | Получает или задает значение, определяющее способ визуализации эффектов DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode) { get; set; } | Получает или задает значение, определяющее способ визуализации фигур DrawingML. |
| [DownsampleOptions](../../aspose.words.saving/pdfsaveoptions/downsampleoptions) { get; set; } | Позволяет указать параметры понижающей дискретизации. |
| [EmbedFullFonts](../../aspose.words.saving/pdfsaveoptions/embedfullfonts) { get; set; } | Управляет тем, как шрифты встраиваются в результирующие документы PDF. |
| [EncryptionDetails](../../aspose.words.saving/pdfsaveoptions/encryptiondetails) { get; set; } | Получает или задает данные для шифрования выходного PDF-документа. |
| [ExportDocumentStructure](../../aspose.words.saving/pdfsaveoptions/exportdocumentstructure) { get; set; } | Получает или задает значение, определяющее, следует ли экспортировать структуру документа. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname) { get; set; } | При значении true имя и версия Aspose.Words встраиваются в создаваемые файлы. Значение по умолчанию: **истинный** . |
| [ExportLanguageToSpanTag](../../aspose.words.saving/pdfsaveoptions/exportlanguagetospantag) { get; set; } | Получает или задает значение, определяющее, следует ли создавать тег «Span» в структуре документа для экспорта языка текста. |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly) { get; set; } | Получает или задает значение, определяющее, какие форматы документов разрешено отображать[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping) . Только по умолчаниюFlatOpc формат документа разрешен для сопоставления. |
| [FontEmbeddingMode](../../aspose.words.saving/pdfsaveoptions/fontembeddingmode) { get; set; } | Определяет режим внедрения шрифта. |
| [HeaderFooterBookmarksExportMode](../../aspose.words.saving/pdfsaveoptions/headerfooterbookmarksexportmode) { get; set; } | Определяет, как экспортируются закладки в верхних/нижних колонтитулах. |
| [ImageColorSpaceExportMode](../../aspose.words.saving/pdfsaveoptions/imagecolorspaceexportmode) { get; set; } | Указывает, как цветовое пространство будет выбрано для изображений в документе PDF. |
| [ImageCompression](../../aspose.words.saving/pdfsaveoptions/imagecompression) { get; set; } | Указывает тип сжатия, который будет использоваться для всех изображений в документе. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode) { get; set; } | Получает или задает значение, определяющее способ визуализации объектов рукописного ввода (InkML). |
| [InterpolateImages](../../aspose.words.saving/pdfsaveoptions/interpolateimages) { get; set; } | Флаг, указывающий, должна ли интерполяция изображения выполняться соответствующим считывателем. Когда`ЛОЖЬ` указан, флаг не записывается в выходной документ и вместо этого используется поведение читателя по умолчанию. |
| [JpegQuality](../../aspose.words.saving/pdfsaveoptions/jpegquality) { get; set; } | Получает или задает значение, определяющее качество изображений JPEG внутри документа PDF. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization) { get; set; } | Получает или задает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойства: **ЛОЖЬ** . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions) { get; set; } | Позволяет указать параметры рендеринга метафайла. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat) { get; set; } | Получает или устанавливает[`NumeralFormat`](../numeralformat) используется для отображения цифр. Европейские цифры используются по умолчанию. |
| [OpenHyperlinksInNewWindow](../../aspose.words.saving/pdfsaveoptions/openhyperlinksinnewwindow) { get; set; } | Получает или задает значение, определяющее, будут ли гиперссылки в выходном Pdf document принудительно открываться в новом окне (или вкладке) браузера. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput) { get; set; } | Флаг указывает, требуется ли оптимизация вывода. этому свойству присвоено значение true. Значение по умолчанию — false. |
| [OutlineOptions](../../aspose.words.saving/pdfsaveoptions/outlineoptions) { get; } | Позволяет указать параметры контура. |
| [PageMode](../../aspose.words.saving/pdfsaveoptions/pagemode) { get; set; } | Указывает, как документ PDF должен отображаться при открытии в программе чтения PDF. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback) { get; set; } | Позволяет управлять сохранением отдельных страниц при экспорте документа в фиксированный формат страницы. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset) { get; set; } | Получает или задает отображаемые страницы. По умолчанию — все страницы документа. |
| [PreblendImages](../../aspose.words.saving/pdfsaveoptions/preblendimages) { get; set; } | Получает или задает значение, определяющее, следует ли предварительно смешивать прозрачные изображения с черным цветом фона. |
| [PreserveFormFields](../../aspose.words.saving/pdfsaveoptions/preserveformfields) { get; set; } | Указывает, сохранять ли поля формы Microsoft Word как поля формы в PDF или преобразовывать их в текст. Значение по умолчанию:`ЛОЖЬ` . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat) { get; set; } | Когда`истинный` , красивые форматы вывода, где это применимо. Значение по умолчанию: **ЛОЖЬ** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback) { get; set; } | Вызывается при сохранении документа и принимает данные о ходе сохранения. |
| override [SaveFormat](../../aspose.words.saving/pdfsaveoptions/saveformat) { get; set; } | Определяет формат, в котором документ будет сохранен, если используется этот объект параметров сохранения.Pdf . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder) { get; set; } | Указывает папку для временных файлов, используемых при сохранении в файл DOC или DOCX. По умолчанию это свойство`нулевой` и никакие временные файлы не используются. |
| [TextCompression](../../aspose.words.saving/pdfsaveoptions/textcompression) { get; set; } | Указывает тип сжатия, который будет использоваться для всего текстового содержимого в документе. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty) { get; set; } | Получает или задает значение, определяющее,[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime) свойство обновляется перед сохранением. Значение по умолчанию — false; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields) { get; set; } | Получает или задает значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы. Значение по умолчанию для этого свойства: **истинный** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty) { get; set; } | Получает или задает значение, определяющее,[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted) свойство обновляется перед сохранением. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty) { get; set; } | Получает или задает значение, определяющее,[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime) свойство обновляется перед сохранением. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent) { get; set; } | Получает или задает значение, определяющее, будет ли содержимое[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag) обновляется перед сохранением. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing) { get; set; } | Получает или задает значение, определяющее, следует ли использовать сглаживание для рендеринга. |
| [UseBookFoldPrintingSettings](../../aspose.words.saving/pdfsaveoptions/usebookfoldprintingsettings) { get; set; } | Получает или задает логическое значение, указывающее, следует ли сохранять документ с использованием макета печати брошюры, , если он указан через[`MultiplePages`](../../aspose.words/pagesetup/multiplepages) . |
| [UseCoreFonts](../../aspose.words.saving/pdfsaveoptions/usecorefonts) { get; set; } | Получает или задает значение, определяющее, следует ли заменять шрифты TrueType Arial, Times New Roman, Courier New и Symbol базовыми шрифтами PDF Type 1. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering) { get; set; } | Получает или задает значение, определяющее, следует ли использовать высококачественные (т.е. медленные) алгоритмы рендеринга. |
| [ZoomBehavior](../../aspose.words.saving/pdfsaveoptions/zoombehavior) { get; set; } | Получает или задает значение, определяющее, какой тип масштабирования следует применять при открытии документа в средстве просмотра PDF. |
| [ZoomFactor](../../aspose.words.saving/pdfsaveoptions/zoomfactor) { get; set; } | Получает или задает значение, определяющее коэффициент масштабирования (в процентах) для документа. |

## Методы

| Имя | Описание |
| --- | --- |
| [Clone](../../aspose.words.saving/pdfsaveoptions/clone)() | Создает глубокий клон этого объекта. |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals)(object) | Определяет, равен ли указанный объект по значению текущему объекту. |

### Примеры

Показывает, как изменить цвет изображения с помощью свойства сохранения параметров.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Создаем объект "PdfSaveOptions", который мы можем передать в метод "Сохранить" документа
// для изменения того, как этот метод преобразует документ в .PDF.
// Установите для свойства «ColorMode» значение «Оттенки серого», чтобы отображать все изображения из документа в черно-белом цвете.
// Размер выходного документа может быть больше с этой настройкой.
// Установите для свойства "ColorMode" значение "Нормальный", чтобы все изображения отображались в цвете.
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

// Создаем объект "PdfSaveOptions", который мы можем передать в метод "Сохранить" документа
// для изменения того, как этот метод преобразует документ в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Установите для свойства "TextCompression" значение "PdfTextCompression.None", чтобы не применять
// сжатие в текст при сохранении документа в PDF.
// Установите для свойства "TextCompression" значение "PdfTextCompression.Flate", чтобы применить сжатие ZIP
// в текст, когда мы сохраняем документ в формате PDF. Чем больше документ, тем большее влияние он окажет.
options.TextCompression = pdfTextCompression;

doc.Save(ArtifactsDir + "PdfSaveOptions.TextCompression.pdf", options);
```

Показывает, как преобразовать весь документ в PDF с тремя уровнями структуры документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем заголовки уровней с 1 по 5.
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

// Создаем объект "PdfSaveOptions", который мы можем передать в метод "Сохранить" документа
// для изменения того, как этот метод преобразует документ в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Выходной PDF-документ будет содержать структуру, которая представляет собой оглавление, в котором перечислены заголовки в теле документа.
// Нажав на запись в этой схеме, мы перейдем к расположению соответствующего заголовка.
// Установите для свойства "HeadingsOutlineLevels" значение "4", чтобы исключить из структуры все заголовки, уровни которых выше 4.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// Если запись схемы имеет последующие записи более высокого уровня между собой и следующей записью того же или более низкого уровня,
// слева от записи появится стрелка. Эта запись является «владельцем» нескольких таких «подзаписей».
// В нашем документе элементы структуры с 5-го уровня заголовка являются подстатьями второго элемента структуры 4-го уровня,
 // статьи 4-го и 5-го уровня заголовков являются подстатьями второй записи 3-го уровня и т.д.
// В схеме мы можем щелкнуть стрелку записи «владелец», чтобы свернуть/развернуть все ее подзаписи.
// Установите для свойства «ExpandedOutlineLevels» значение «2», чтобы автоматически расширять все элементы уровня заголовка 2 и нижнего уровня структуры
 // и свернуть все записи уровня и 3 и выше при открытии документа.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### Смотрите также

* class [FixedPageSaveOptions](../fixedpagesaveoptions)
* пространство имен [Aspose.Words.Saving](../../aspose.words.saving)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
