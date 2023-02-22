---
title: Class PclSaveOptions
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Saving.PclSaveOptions сорт. Может использоваться для указания дополнительных параметров при сохранении документа вPcl формат.
type: docs
weight: 5120
url: /ru/net/aspose.words.saving/pclsaveoptions/
---
## PclSaveOptions class

Может использоваться для указания дополнительных параметров при сохранении документа вPcl формат.

```csharp
public class PclSaveOptions : FixedPageSaveOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [PclSaveOptions](pclsaveoptions/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Возвращает или задает логическое значение, указывающее, разрешать ли встраивание шрифтов с помощью PostScript layouts при встраивании шрифтов TrueType в документ после его сохранения. Значение по умолчанию: **ЛОЖЬ** . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | Получает или задает значение, определяющее способ отображения цветов. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Получает или задает пользовательский местный часовой пояс, используемый для полей даты/времени. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Получает или задает путь к шаблону по умолчанию (включая имя файла). Значение по умолчанию для этого свойства: **пустой строки** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Получает или задает значение, определяющее способ визуализации 3D-эффектов. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Получает или задает значение, определяющее способ визуализации эффектов DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Получает или задает значение, определяющее способ визуализации фигур DrawingML. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | При значении true имя и версия Aspose.Words встраиваются в создаваемые файлы. Значение по умолчанию: **истинный** . |
| [FallbackFontName](../../aspose.words.saving/pclsaveoptions/fallbackfontname/) { get; set; } | Имя шрифта, который будет использоваться , если ожидаемый шрифт не найден в коллекциях принтеров и встроенных шрифтов. |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly/) { get; set; } | Получает или задает значение, определяющее, какие форматы документов разрешено отображать[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Только по умолчаниюFlatOpc формат документа разрешен для сопоставления. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Получает или задает значение, определяющее способ визуализации объектов рукописного ввода (InkML). |
| [JpegQuality](../../aspose.words.saving/fixedpagesaveoptions/jpegquality/) { get; set; } | Получает или задает значение, определяющее качество изображений JPEG внутри HTML-документа. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Получает или задает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойства: **ЛОЖЬ** . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/) { get; set; } | Позволяет указать параметры рендеринга метафайла. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | Получает или устанавливает[`NumeralFormat`](../numeralformat/) используется для отображения цифр. Европейские цифры используются по умолчанию. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput/) { get; set; } | Флаг указывает, требуется ли оптимизация вывода. этому свойству присвоено значение true. Значение по умолчанию — false. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Позволяет управлять сохранением отдельных страниц при экспорте документа в фиксированный формат страницы. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset/) { get; set; } | Получает или задает отображаемые страницы. По умолчанию — все страницы документа. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Когда`истинный` , красивые форматы вывода, где это применимо. Значение по умолчанию: **ЛОЖЬ** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Вызывается при сохранении документа и принимает данные о ходе сохранения. |
| [RasterizeTransformedElements](../../aspose.words.saving/pclsaveoptions/rasterizetransformedelements/) { get; set; } | Получает или задает значение, определяющее, следует ли растрировать сложные преобразованные элементы перед сохранением в документ PCL. Значение по умолчанию:`истинный` . |
| override [SaveFormat](../../aspose.words.saving/pclsaveoptions/saveformat/) { get; set; } | Определяет формат, в котором документ будет сохранен, если используется этот объект параметров сохранения.Pcl . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Указывает папку для временных файлов, используемых при сохранении в файл DOC или DOCX. По умолчанию это свойство`нулевой` и никакие временные файлы не используются. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Получает или задает значение, определяющее,[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) свойство обновляется перед сохранением. Значение по умолчанию — false; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Получает или задает значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы. Значение по умолчанию для этого свойства: **истинный** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Получает или задает значение, определяющее,[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) свойство обновляется перед сохранением. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Получает или задает значение, определяющее,[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) свойство обновляется перед сохранением. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent/) { get; set; } | Получает или задает значение, определяющее, будет ли содержимое[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) обновляется перед сохранением. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Получает или задает значение, определяющее, следует ли использовать сглаживание для рендеринга. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Получает или задает значение, определяющее, следует ли использовать высококачественные (т.е. медленные) алгоритмы рендеринга. |

## Методы

| Имя | Описание |
| --- | --- |
| [AddPrinterFont](../../aspose.words.saving/pclsaveoptions/addprinterfont/)(string, string) | Добавляет информацию о шрифте, загруженном производителем на принтер. |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(object) | Определяет, равен ли указанный объект по значению текущему объекту. |

### Примеры

Показывает, как растрировать сложные элементы при сохранении документа в PCL.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

PclSaveOptions saveOptions = new PclSaveOptions
{
    SaveFormat = SaveFormat.Pcl,
    RasterizeTransformedElements = true
};

doc.Save(ArtifactsDir + "PclSaveOptions.RasterizeElements.pcl", saveOptions);
```

### Смотрите также

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)


