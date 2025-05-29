---
title: RtfSaveOptions Class
linktitle: RtfSaveOptions
articleTitle: RtfSaveOptions
second_title: Aspose.Words для .NET
description: Откройте для себя Aspose.Words.RtfSaveOptions, чтобы улучшить ваш опыт сохранения документов. Настройте вывод RTF с помощью расширенных настроек для оптимальных результатов.
type: docs
weight: 6370
url: /ru/net/aspose.words.saving/rtfsaveoptions/
---
## RtfSaveOptions class

Может использоваться для указания дополнительных параметров при сохранении документа вRtf формат.

Чтобы узнать больше, посетите[Укажите параметры сохранения](https://docs.aspose.com/words/net/specify-save-options/) документальная статья.

```csharp
public class RtfSaveOptions : SaveOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [RtfSaveOptions](rtfsaveoptions/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Возвращает или задает логическое значение, указывающее, разрешать ли встраивание шрифтов с контурами PostScript при встраивании шрифтов TrueType в документ при его сохранении. Значение по умолчанию:`ЛОЖЬ` . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Возвращает или задает пользовательский локальный часовой пояс, используемый для полей даты/времени. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Возвращает или задает путь к шаблону по умолчанию (включая имя файла). Значение по умолчанию для этого свойства:**пустая строка** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Возвращает или задает значение, определяющее способ визуализации 3D-эффектов. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Возвращает или задает значение, определяющее способ визуализации эффектов DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Возвращает или задает значение, определяющее способ визуализации фигур DrawingML. |
| [ExportCompactSize](../../aspose.words.saving/rtfsaveoptions/exportcompactsize/) { get; set; } | Позволяет уменьшить размер выходных RTF-документов, но если они содержат текст RTL (справа налево), он будет отображаться неправильно. Значение по умолчанию:`ЛОЖЬ` . |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Когда`истинный` , приводит к внедрению имени и версии Aspose.Words в создаваемые файлы. Значение по умолчанию:`истинный` . |
| [ExportImagesForOldReaders](../../aspose.words.saving/rtfsaveoptions/exportimagesforoldreaders/) { get; set; } | Указывает, записываются ли ключевые слова для «старых читателей» в RTF или нет. Это может существенно повлиять на размер документа RTF. Значение по умолчанию:`истинный` . |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Возвращает или задает значение, определяющее способ визуализации объектов рукописного ввода (InkML). |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Возвращает или задает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойства:`ЛОЖЬ` . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Когда`истинный` , красивые форматы вывода, где это применимо. Значение по умолчанию:`ЛОЖЬ` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Вызывается во время сохранения документа и принимает данные о ходе сохранения. |
| override [SaveFormat](../../aspose.words.saving/rtfsaveoptions/saveformat/) { get; set; } | Указывает формат, в котором будет сохранен документ, если используется этот объект параметров сохранения. Может быть толькоRtf . |
| [SaveImagesAsWmf](../../aspose.words.saving/rtfsaveoptions/saveimagesaswmf/) { get; set; } | Когда`истинный` все изображения будут сохранены как WMF. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Указывает папку для временных файлов, используемых при сохранении в файл DOC или DOCX. По умолчанию это свойство`нулевой` и временные файлы не используются. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Определяет, будут ли изменяться атрибуты шрифта в соответствии с используемым кодом символа. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Возвращает или задает значение, определяющее, является ли[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) свойство обновляется перед сохранением. Значение по умолчанию:`ЛОЖЬ` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Возвращает или задает значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы. Значение по умолчанию для этого свойства:`истинный` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Возвращает или задает значение, определяющее, является ли[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) свойство обновляется перед сохранением. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Возвращает или задает значение, определяющее, является ли[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) свойство обновляется перед сохранением. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Возвращает или задает значение, определяющее, следует ли использовать сглаживание при рендеринге. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Возвращает или задает значение, определяющее, следует ли использовать высококачественные (т. е. медленные) алгоритмы рендеринга. |

## Примеры

Показывает, как сохранить документ в формате .rtf с пользовательскими параметрами.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Создаем объект «RtfSaveOptions» для передачи методу «Save» документа, чтобы изменить способ сохранения в формате RTF.
RtfSaveOptions options = new RtfSaveOptions();

Assert.AreEqual(SaveFormat.Rtf, options.SaveFormat);

// Установите свойство "ExportCompactSize" в значение "true" для
// уменьшить размер сохраненного документа за счет совместимости с текстом, написанным справа налево.
options.ExportCompactSize = true;

// Установите свойство "ExportImagesFotOldReaders" в значение "true", чтобы использовать дополнительные ключевые слова и гарантировать, что наш документ
// совместимо с программами чтения до Microsoft Word 97 и WordPad.
// Установите свойство "ExportImagesFotOldReaders" в значение "false", чтобы уменьшить размер документа,
// но не позволяйте старым читателям читать любые неметафайловые или BMP-изображения, которые может содержать документ.
options.ExportImagesForOldReaders = exportImagesForOldReaders;

doc.Save(ArtifactsDir + "RtfSaveOptions.ExportImages.rtf", options);
```

### Смотрите также

* class [SaveOptions](../saveoptions/)
* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
