---
title: HtmlLoadOptions
second_title: Справочник по API Aspose.Words для .NET
description: Позволяет указать дополнительные параметры при загрузке HTML-документа в объектDocument../aspose.words/document.
type: docs
weight: 3370
url: /ru/net/aspose.words.loading/htmlloadoptions/
---
## HtmlLoadOptions class

Позволяет указать дополнительные параметры при загрузке HTML-документа в объект[`Document`](../../aspose.words/document).

```csharp
public class HtmlLoadOptions : LoadOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [HtmlLoadOptions](htmlloadoptions#constructor)() | Инициализирует новый экземпляр этого класса со значениями по умолчанию. |
| [HtmlLoadOptions](htmlloadoptions#constructor_2)(string) | Ярлык для инициализации нового экземпляра этого класса с указанным паролем для загрузки зашифрованного документа. |
| [HtmlLoadOptions](htmlloadoptions#constructor_1)(LoadFormat, string, string) | Ярлык для инициализации нового экземпляра этого класса со свойствами, установленными на указанные значения. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri) { get; set; } | Получает или задает строку, которая будет использоваться для преобразования относительных URI, найденных в документе, в абсолютные URI, когда это необходимо. Может быть null или пустой строкой. Значение по умолчанию равно нулю. |
| [BlockImportMode](../../aspose.words.loading/htmlloadoptions/blockimportmode) { get; set; } | Получает или задает значение, указывающее, как импортируются свойства элементов уровня блока. Значение по умолчанию:Merge. |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng) { get; set; } | Получает или задает, следует ли преобразовывать метафайл (WmfилиEmf) изображения вPngформат изображения. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath) { get; set; } | Получает или задает, следует ли преобразовывать фигуры с помощью EquationXML в объекты Office Math. |
| [ConvertSvgToEmf](../../aspose.words.loading/htmlloadoptions/convertsvgtoemf) { get; set; } | Получает или задает значение, указывающее, следует ли преобразовывать загруженные изображения SVG в формат EMF. Значение по умолчанию:` false` и, по возможности, загруженные изображения SVG сохраняются как есть без преобразования. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding) { get; set; } | Получает или задает кодировку, которая будет использоваться для загрузки документа HTML, TXT или CHM, если кодировка не указана внутри документа . Может быть нулевым. Значение по умолчанию равно нулю. |
| [FlatOpcXmlMappingOnly](../../aspose.words.loading/loadoptions/flatopcxmlmappingonly) { get; set; } | Получает или задает значение, определяющее, какие форматы документов разрешено отображать с помощью[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping). По умолчанию только формат документаFlatOpcразрешен для сопоставления. |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings) { get; set; } | Позволяет задать настройки шрифта документа. |
| [IgnoreNoscriptElements](../../aspose.words.loading/htmlloadoptions/ignorenoscriptelements) { get; set; } | Получает или задает значение, указывающее, следует ли игнорировать &lt;noscript&gt; HTML-элементы. Значение по умолчанию:` false` . |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences) { get; } | Получает языковые настройки, которые будут использоваться при загрузке документа. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat) { get; set; } | Задает формат загружаемого документа. По умолчанию:Auto. |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion) { get; set; } | Позволяет указать, что процесс загрузки документа должен соответствовать конкретной версии MS Word. Значение по умолчанию:Word2019 |
| [Password](../../aspose.words.loading/loadoptions/password) { get; set; } | Получает или задает пароль для открытия зашифрованного документа. Может быть null или пустой строкой. Значение по умолчанию равно нулю. |
| [PreferredControlType](../../aspose.words.loading/htmlloadoptions/preferredcontroltype) { get; set; } | Получает или задает предпочтительный тип узлов документа, которые будут представлять импортированные &lt;input&gt; и &lt;выбрать&gt; элементы. Значение по умолчанию:FormField. |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield) { get; set; } | Получает или задает, следует ли сохранять поле INCLUDEPICTURE при чтении форматов Microsoft Word. Значение по умолчанию — false. |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback) { get; set; } | Вызывается при загрузке документа и принимает данные о ходе загрузки. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback) { get; set; } | Позволяет управлять загрузкой внешних ресурсов (изображений, таблиц стилей) при импорте документа из HTML, MHTML. |
| [SupportVml](../../aspose.words.loading/htmlloadoptions/supportvml) { get; set; } | Получает или задает значение, указывающее, поддерживать ли образы VML. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder) { get; set; } | Позволяет использовать временные файлы при чтении документа. По умолчанию это свойство` null` и временные файлы не используются. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields) { get; set; } | Указывает, обновлять ли поля с атрибутом` dirty` . |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback) { get; set; } | Вызывается во время операции загрузки, когда обнаруживается проблема, которая может привести к потере точности данных или форматирования. |
| [WebRequestTimeout](../../aspose.words.loading/htmlloadoptions/webrequesttimeout) { get; set; } | Количество миллисекунд ожидания до истечения времени ожидания веб-запроса. Значение по умолчанию — 100000 миллисекунд (100 секунд). |

### Смотрите также

* class [LoadOptions](../loadoptions)
* namespace [Aspose.Words.Loading](../../aspose.words.loading)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
