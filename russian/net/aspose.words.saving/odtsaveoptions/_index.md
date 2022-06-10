---
title: OdtSaveOptions
second_title: Справочник по API Aspose.Words для .NET
description: Может использоваться для указания дополнительных параметров при сохранении документа в форматеOdtили Ottформат.
type: docs
weight: 5000
url: /ru/net/aspose.words.saving/odtsaveoptions/
---
## OdtSaveOptions class

Может использоваться для указания дополнительных параметров при сохранении документа в форматеOdtили Ottформат.

```csharp
public class OdtSaveOptions : SaveOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [OdtSaveOptions](odtsaveoptions#constructor)() | Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа в форматеOdt. |
| [OdtSaveOptions](odtsaveoptions#constructor_1)(SaveFormat) | Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа вOdtили Ottформат. |
| [OdtSaveOptions](odtsaveoptions#constructor_2)(string) | Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа в форматеOdt зашифровано паролем. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts) { get; set; } | Получает или задает логическое значение, указывающее, разрешить ли встраивание шрифтов с контурами PostScript при встраивании шрифтов TrueType в документ после его сохранения. Значение по умолчанию: **false** . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo) { get; set; } | Получает или задает пользовательский местный часовой пояс, используемый для полей даты/времени. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate) { get; set; } | Получает или задает путь к шаблону по умолчанию (включая имя файла). Значение по умолчанию для этого свойства: **пустая строка** (Empty). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode) { get; set; } | Получает или задает значение, определяющее способ визуализации 3D-эффектов. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode) { get; set; } | Получает или задает значение, определяющее способ визуализации эффектов DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode) { get; set; } | Получает или задает значение, определяющее способ визуализации фигур DrawingML. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname) { get; set; } | При значении true имя и версия Aspose.Words встраиваются в создаваемые файлы. Значение по умолчанию: **true** . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly) { get; set; } | Получает или задает значение, определяющее, какие форматы документов разрешено отображать с помощью[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping). По умолчанию только формат документаFlatOpcразрешен для сопоставления. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode) { get; set; } | Получает или задает значение, определяющее способ визуализации объектов рукописного ввода (InkML). |
| [IsStrictSchema11](../../aspose.words.saving/odtsaveoptions/isstrictschema11) { get; set; } | Указывает, должен ли экспорт строго соответствовать спецификации ODT 1.1. OOo 3.0 правильно отображает файлы, если они содержат элементы и атрибуты ODT 1.2. Используйте "false" для этой цели или "true" для строгого соответствия спецификации 1.1. Значение по умолчанию: **false** . |
| [MeasureUnit](../../aspose.words.saving/odtsaveoptions/measureunit) { get; set; } | Позволяет указать единицы измерения для применения к содержимому документа. Значение по умолчанию:Centimeters |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization) { get; set; } | Получает или задает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойства: **false** . |
| [Password](../../aspose.words.saving/odtsaveoptions/password) { get; set; } | Получает или задает пароль для шифрования документа. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat) { get; set; } | Когда` true` , вывод форматируется, где это применимо. Значение по умолчанию: **false** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback) { get; set; } | Вызывается при сохранении документа и принимает данные о ходе сохранения. |
| override [SaveFormat](../../aspose.words.saving/odtsaveoptions/saveformat) { get; set; } | Указывает формат, в котором будет сохранен документ, если используется этот объект параметров сохранения. Может бытьOdtилиOtt. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder) { get; set; } | Указывает папку для временных файлов, используемых при сохранении в файл DOC или DOCX. По умолчанию это свойство` null` и временные файлы не используются. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty) { get; set; } | Получает или задает значение, определяющее, обновляется ли свойство[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime)перед сохранением. Значение по умолчанию - false; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields) { get; set; } | Получает или задает значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы. Значение по умолчанию для этого свойства: **true** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty) { get; set; } | Получает или задает значение, определяющее, обновляется ли свойство[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted)перед сохранением. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty) { get; set; } | Получает или задает значение, определяющее, обновляется ли свойство[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime)перед сохранением. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent) { get; set; } | Получает или задает значение, определяющее, будет ли содержимое[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag)обновляться перед сохранением. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing) { get; set; } | Получает или задает значение, определяющее, следует ли использовать сглаживание для визуализации. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering) { get; set; } | Получает или задает значение, определяющее, следует ли использовать высококачественные (т.е. медленные) алгоритмы рендеринга. |

### Примечания

На данный момент предоставляет только[`SaveFormat`](./saveformat)свойство, но в будущем будут добавлены другие параметры, такие как пароль шифрования или настройки цифровой подписи.

### Примеры

Показывает, как привести сохраненный документ в соответствие со старой схемой ODT.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

 // Когда мы экспортируем документ в .odt, мы можем использовать объект OdtSaveOptions, чтобы изменить способ сохранения документа.
 // Мы можем установить для свойства "MeasureUnit" значение "OdtSaveMeasureUnit.Centimeters"
// для определения содержимого, такого как параметры стиля, с использованием метрической системы, которую использует Open Office. 
 // Мы можем установить для свойства "MeasureUnit" значение "OdtSaveMeasureUnit.Inches"
 // для определения содержимого, такого как параметры стиля, с использованием имперской системы, которую использует Microsoft Word.
OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = odtSaveMeasureUnit
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

Показывает, как использовать различные единицы измерения для определения параметров стиля сохраненного документа ODT.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

 // Когда мы экспортируем документ в .odt, мы можем использовать объект OdtSaveOptions, чтобы изменить способ сохранения документа.
 // Мы можем установить для свойства "MeasureUnit" значение "OdtSaveMeasureUnit.Centimeters"
// для определения содержимого, такого как параметры стиля, с использованием метрической системы, которую использует Open Office. 
 // Мы можем установить для свойства "MeasureUnit" значение "OdtSaveMeasureUnit.Inches"
 // для определения содержимого, такого как параметры стиля, с использованием имперской системы, которую использует Microsoft Word.
OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = odtSaveMeasureUnit
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Смотрите также

* class [SaveOptions](../saveoptions)
* namespace [Aspose.Words.Saving](../../aspose.words.saving)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
