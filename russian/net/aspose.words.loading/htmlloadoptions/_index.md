---
title: HtmlLoadOptions
second_title: Справочник по API Aspose.Words для .NET
description: Позволяет указать дополнительные параметры при загрузке HTMLдокумента вDocument../aspose.words/document/ объект.
type: docs
weight: 3420
url: /ru/net/aspose.words.loading/htmlloadoptions/
---
## HtmlLoadOptions class

Позволяет указать дополнительные параметры при загрузке HTML-документа в[`Document`](../../aspose.words/document/) объект.

```csharp
public class HtmlLoadOptions : LoadOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [HtmlLoadOptions](htmlloadoptions/#constructor)() | Инициализирует новый экземпляр этого класса со значениями по умолчанию. |
| [HtmlLoadOptions](htmlloadoptions/#constructor_2)(string) | Ярлык для инициализации нового экземпляра этого класса с указанным паролем для загрузки зашифрованного документа. |
| [HtmlLoadOptions](htmlloadoptions/#constructor_1)(LoadFormat, string, string) | Ярлык для инициализации нового экземпляра этого класса со свойствами, установленными на указанные значения. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Получает или задает строку, которая будет использоваться для преобразования относительных URI, найденных в документе, в абсолютные URI, когда это необходимо. Может быть нулевой или пустой строкой. Значение по умолчанию — null. |
| [BlockImportMode](../../aspose.words.loading/htmlloadoptions/blockimportmode/) { get; set; } | Получает или задает значение, указывающее, как импортируются свойства элементов уровня блока. Значение по умолчанию:Merge . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Получает или задает, следует ли преобразовывать метафайл (Wmf или жеEmf ) изображения вPng формат изображения. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Получает или задает, следует ли преобразовывать фигуры с помощью EquationXML в объекты Office Math. |
| [ConvertSvgToEmf](../../aspose.words.loading/htmlloadoptions/convertsvgtoemf/) { get; set; } | Получает или задает значение, указывающее, следует ли преобразовывать загруженные изображения SVG в формат EMF. Значение по умолчанию:`ЛОЖЬ` и, если возможно, загруженные изображения SVG сохраняются как есть без преобразования. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Получает или задает кодировку, которая будет использоваться для загрузки документа HTML, TXT или CHM, если кодировка не указана внутри документа. Может быть нулевым. Значение по умолчанию — null. |
| [FlatOpcXmlMappingOnly](../../aspose.words.loading/loadoptions/flatopcxmlmappingonly/) { get; set; } | Получает или задает значение, определяющее, какие форматы документов разрешено отображать[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Только по умолчаниюFlatOpc формат документа разрешен для сопоставления. |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Позволяет указать настройки шрифта документа. |
| [IgnoreNoscriptElements](../../aspose.words.loading/htmlloadoptions/ignorenoscriptelements/) { get; set; } | Получает или задает значение, указывающее, следует ли игнорировать HTML-элементы &lt;noscript&gt;. Значение по умолчанию:`ЛОЖЬ` . |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Получает языковые настройки, которые будут использоваться при загрузке документа. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Указывает формат загружаемого документа. Значение по умолчанию:Auto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Позволяет указать, что процесс загрузки документа должен соответствовать конкретной версии MS Word. Значение по умолчанию:Word2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Получает или задает пароль для открытия зашифрованного документа. Может быть нулевым или пустой строкой. Значение по умолчанию — null. |
| [PreferredControlType](../../aspose.words.loading/htmlloadoptions/preferredcontroltype/) { get; set; } | Получает или задает предпочтительный тип узлов документа, которые будут представлять импортированные элементы &lt;input&gt; и &lt;select&gt;. Значение по умолчанию:FormField . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Получает или задает, следует ли сохранять поле INCLUDEPICTURE при чтении форматов Microsoft Word. Значение по умолчанию — false. |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Вызывается при загрузке документа и принимает данные о ходе загрузки. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Позволяет управлять загрузкой внешних ресурсов (изображений, таблиц стилей) при импорте документа из HTML, MHTML. |
| [SupportVml](../../aspose.words.loading/htmlloadoptions/supportvml/) { get; set; } | Получает или задает значение, указывающее, поддерживать ли образы VML. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Позволяет использовать временные файлы при чтении документа. По умолчанию это свойство`нулевой` и никакие временные файлы не используются. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Указывает, обновлять ли поля с`грязный` атрибут. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Вызывается во время операции загрузки при обнаружении проблемы, которая может привести к потере точности данных или форматирования. |
| [WebRequestTimeout](../../aspose.words.loading/htmlloadoptions/webrequesttimeout/) { get; set; } | Количество миллисекунд ожидания до истечения времени ожидания веб-запроса. Значение по умолчанию — 100000 миллисекунд (100 секунд). . |

### Смотрите также

* class [LoadOptions](../loadoptions/)
* пространство имен [Aspose.Words.Loading](../../aspose.words.loading/)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
