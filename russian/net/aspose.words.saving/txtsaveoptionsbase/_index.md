---
title: Class TxtSaveOptionsBase
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Saving.TxtSaveOptionsBase сорт. Базовый класс для указания дополнительных параметров при сохранении документа в текстовом формате.
type: docs
weight: 5390
url: /ru/net/aspose.words.saving/txtsaveoptionsbase/
---
## TxtSaveOptionsBase class

Базовый класс для указания дополнительных параметров при сохранении документа в текстовом формате.

```csharp
public abstract class TxtSaveOptionsBase : SaveOptions
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Возвращает или задает логическое значение, указывающее, разрешать ли встраивание шрифтов с помощью PostScript layouts при встраивании шрифтов TrueType в документ после его сохранения. Значение по умолчанию: **ЛОЖЬ** . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Получает или задает пользовательский местный часовой пояс, используемый для полей даты/времени. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Получает или задает путь к шаблону по умолчанию (включая имя файла). Значение по умолчанию для этого свойства: **пустой строки** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Получает или задает значение, определяющее способ визуализации 3D-эффектов. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Получает или задает значение, определяющее способ визуализации эффектов DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Получает или задает значение, определяющее способ визуализации фигур DrawingML. |
| [Encoding](../../aspose.words.saving/txtsaveoptionsbase/encoding/) { get; set; } | Указывает кодировку, используемую при экспорте в текстовые форматы. Значение по умолчанию: **Кодировка.UTF8** . |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | При значении true имя и версия Aspose.Words встраиваются в создаваемые файлы. Значение по умолчанию: **истинный** . |
| [ExportHeadersFootersMode](../../aspose.words.saving/txtsaveoptionsbase/exportheadersfootersmode/) { get; set; } | Указывает способ экспорта верхних и нижних колонтитулов в текстовые форматы. Значение по умолчанию:PrimaryOnly . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly/) { get; set; } | Получает или задает значение, определяющее, какие форматы документов разрешено отображать[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Только по умолчаниюFlatOpc формат документа разрешен для сопоставления. |
| [ForcePageBreaks](../../aspose.words.saving/txtsaveoptionsbase/forcepagebreaks/) { get; set; } | Позволяет указать, следует ли сохранять разрывы страниц при экспорте. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Получает или задает значение, определяющее способ визуализации объектов рукописного ввода (InkML). |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Получает или задает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойства: **ЛОЖЬ** . |
| [ParagraphBreak](../../aspose.words.saving/txtsaveoptionsbase/paragraphbreak/) { get; set; } | Указывает строку, используемую в качестве разрыва абзаца при экспорте в текстовые форматы. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Когда`истинный` , красивые форматы вывода, где это применимо. Значение по умолчанию: **ЛОЖЬ** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Вызывается при сохранении документа и принимает данные о ходе сохранения. |
| abstract [SaveFormat](../../aspose.words.saving/saveoptions/saveformat/) { get; set; } | Указывает формат, в котором документ будет сохранен, если используется этот объект параметров сохранения. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Указывает папку для временных файлов, используемых при сохранении в файл DOC или DOCX. По умолчанию это свойство`нулевой` и никакие временные файлы не используются. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Получает или задает значение, определяющее,[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) свойство обновляется перед сохранением. Значение по умолчанию — false; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Получает или задает значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы. Значение по умолчанию для этого свойства: **истинный** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Получает или задает значение, определяющее,[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) свойство обновляется перед сохранением. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Получает или задает значение, определяющее,[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) свойство обновляется перед сохранением. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent/) { get; set; } | Получает или задает значение, определяющее, будет ли содержимое[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) обновляется перед сохранением. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Получает или задает значение, определяющее, следует ли использовать сглаживание для рендеринга. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Получает или задает значение, определяющее, следует ли использовать высококачественные (т.е. медленные) алгоритмы рендеринга. |

### Примеры

Показывает, как сохранить документ .txt с настраиваемым разрывом абзаца.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");
builder.Write("Paragraph 3.");

// Создаем объект "TxtSaveOptions", который мы можем передать в метод "Сохранить" документа
// чтобы изменить способ сохранения документа в виде открытого текста.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

Assert.AreEqual(SaveFormat.Text, txtSaveOptions.SaveFormat);

// Установите для «ParagraphBreak» пользовательское значение, которое мы хотим поместить в конце каждого абзаца.
txtSaveOptions.ParagraphBreak = " End of paragraph.\n\n\t";

doc.Save(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt");

Assert.AreEqual("Paragraph 1. End of paragraph.\n\n\t" +
                "Paragraph 2. End of paragraph.\n\n\t" +
                "Paragraph 3. End of paragraph.\n\n\t", docText);
```

### Смотрите также

* class [SaveOptions](../saveoptions/)
* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)


