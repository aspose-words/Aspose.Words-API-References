---
title: TxtLoadOptions
second_title: Справочник по API Aspose.Words для .NET
description: Позволяет указать дополнительные параметры при загрузкеTextдокумента вDocument../aspose.words/documentобъект.
type: docs
weight: 3480
url: /ru/net/aspose.words.loading/txtloadoptions/
---
## TxtLoadOptions class

Позволяет указать дополнительные параметры при загрузкеTextдокумента в[`Document`](../../aspose.words/document)объект.

```csharp
public class TxtLoadOptions : LoadOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [TxtLoadOptions](txtloadoptions)() | Инициализирует новый экземпляр этого класса со значениями по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri) { get; set; } | Получает или задает строку, которая будет использоваться для преобразования относительных URI, найденных в документе, в абсолютные URI, когда это необходимо. Может быть null или пустой строкой. Значение по умолчанию равно нулю. |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng) { get; set; } | Получает или задает, следует ли преобразовывать метафайл (WmfилиEmf) изображения вPngформат изображения. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath) { get; set; } | Получает или задает, следует ли преобразовывать фигуры с помощью EquationXML в объекты Office Math. |
| [DetectNumberingWithWhitespaces](../../aspose.words.loading/txtloadoptions/detectnumberingwithwhitespaces) { get; set; } | Позволяет указать, как распознаются элементы нумерованного списка при импорте документа из обычного текстового формата. Значение по умолчанию — true. |
| [DocumentDirection](../../aspose.words.loading/txtloadoptions/documentdirection) { get; set; } | Получает или задает направление документа. Значение по умолчанию:LeftToRight. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding) { get; set; } | Получает или задает кодировку, которая будет использоваться для загрузки документа HTML, TXT или CHM, если кодировка не указана внутри документа . Может быть нулевым. Значение по умолчанию равно нулю. |
| [FlatOpcXmlMappingOnly](../../aspose.words.loading/loadoptions/flatopcxmlmappingonly) { get; set; } | Получает или задает значение, определяющее, какие форматы документов разрешено отображать с помощью[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping). По умолчанию только формат документаFlatOpcразрешен для сопоставления. |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings) { get; set; } | Позволяет задать настройки шрифта документа. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences) { get; } | Получает языковые настройки, которые будут использоваться при загрузке документа. |
| [LeadingSpacesOptions](../../aspose.words.loading/txtloadoptions/leadingspacesoptions) { get; set; } | Получает или задает предпочтительный вариант обработки начального пробела. Значение по умолчанию:ConvertToIndent. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat) { get; set; } | Задает формат загружаемого документа. По умолчанию:Auto. |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion) { get; set; } | Позволяет указать, что процесс загрузки документа должен соответствовать конкретной версии MS Word. Значение по умолчанию:Word2019 |
| [Password](../../aspose.words.loading/loadoptions/password) { get; set; } | Получает или задает пароль для открытия зашифрованного документа. Может быть null или пустой строкой. Значение по умолчанию равно нулю. |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield) { get; set; } | Получает или задает, следует ли сохранять поле INCLUDEPICTURE при чтении форматов Microsoft Word. Значение по умолчанию — false. |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback) { get; set; } | Вызывается при загрузке документа и принимает данные о ходе загрузки. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback) { get; set; } | Позволяет управлять загрузкой внешних ресурсов (изображений, таблиц стилей) при импорте документа из HTML, MHTML. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder) { get; set; } | Позволяет использовать временные файлы при чтении документа. По умолчанию это свойство` null` и временные файлы не используются. |
| [TrailingSpacesOptions](../../aspose.words.loading/txtloadoptions/trailingspacesoptions) { get; set; } | Получает или задает предпочтительный вариант обработки завершающего пробела. Значение по умолчанию:Trim. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields) { get; set; } | Указывает, обновлять ли поля с атрибутом` dirty` . |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback) { get; set; } | Вызывается во время операции загрузки, когда обнаруживается проблема, которая может привести к потере точности данных или форматирования. |

### Смотрите также

* class [LoadOptions](../loadoptions)
* namespace [Aspose.Words.Loading](../../aspose.words.loading)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
