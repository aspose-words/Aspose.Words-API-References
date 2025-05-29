---
title: HtmlLoadOptions Class
linktitle: HtmlLoadOptions
articleTitle: HtmlLoadOptions
second_title: Aspose.Words для .NET
description: Откройте для себя Aspose.Words.Loading.HtmlLoadOptions, чтобы улучшить загрузку HTML-документа в объект Document с помощью настраиваемых параметров для оптимальной производительности.
type: docs
weight: 4070
url: /ru/net/aspose.words.loading/htmlloadoptions/
---
## HtmlLoadOptions class

Позволяет указать дополнительные параметры при загрузке HTML-документа в[`Document`](../../aspose.words/document/) объект.

Чтобы узнать больше, посетите[Укажите параметры загрузки](https://docs.aspose.com/words/net/specify-load-options/) документальная статья.

```csharp
public class HtmlLoadOptions : LoadOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [HtmlLoadOptions](htmlloadoptions/#constructor)() | Инициализирует новый экземпляр этого класса со значениями по умолчанию. |
| [HtmlLoadOptions](htmlloadoptions/#constructor_2)(*string*) | Ярлык для инициализации нового экземпляра этого класса с указанным паролем для загрузки зашифрованного документа. |
| [HtmlLoadOptions](htmlloadoptions/#constructor_1)(*[LoadFormat](../../aspose.words/loadformat/), string, string*) | Ярлык для инициализации нового экземпляра этого класса со свойствами, установленными на указанные значения. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Возвращает или задает строку, которая будет использоваться для преобразования относительных URI, найденных в документе, в абсолютные URI при необходимости. Может быть`нулевой` или пустая строка. По умолчанию`нулевой` . |
| [BlockImportMode](../../aspose.words.loading/htmlloadoptions/blockimportmode/) { get; set; } | Возвращает или задает значение, указывающее, как импортируются свойства элементов уровня блока. Значение по умолчанию:Merge . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Возвращает или задает, следует ли преобразовывать метафайл (Wmf илиEmf ) изображения вPngформат изображения. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Возвращает или задает, следует ли преобразовывать фигуры с EquationXML в объекты Office Math. |
| [ConvertSvgToEmf](../../aspose.words.loading/htmlloadoptions/convertsvgtoemf/) { get; set; } | Возвращает или задает значение, указывающее, следует ли преобразовывать загруженные изображения SVG в формат EMF. Значение по умолчанию:`ЛОЖЬ` и, если возможно, загруженные SVG-изображения сохраняются как есть без конвертации. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Возвращает или задает кодировку, которая будет использоваться для загрузки документа HTML, TXT или CHM, если кодировка не указана внутри документа. Может быть`нулевой` . По умолчанию`нулевой` . |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Позволяет указать настройки шрифта документа. |
| [IgnoreNoscriptElements](../../aspose.words.loading/htmlloadoptions/ignorenoscriptelements/) { get; set; } | Возвращает или задает значение, указывающее, следует ли игнорировать элементы HTML &lt;noscript&gt;. Значение по умолчанию:`ЛОЖЬ` . |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | Указывает, следует ли игнорировать данные OLE. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Получает языковые настройки, которые будут использоваться при загрузке документа. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Указывает формат документа для загрузки. Значение по умолчанию:Auto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Позволяет указать, что процесс загрузки документа должен соответствовать определенной версии MS Word. Значение по умолчанию:Word2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Возвращает или задает пароль для открытия зашифрованного документа. Может быть`нулевой` или пустая строка. По умолчанию`нулевой` . |
| [PreferredControlType](../../aspose.words.loading/htmlloadoptions/preferredcontroltype/) { get; set; } | Возвращает или задает предпочтительный тип узлов документа, которые будут представлять импортированные элементы &lt;input&gt; и &lt;select&gt;. Значение по умолчанию:FormField . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Возвращает или задает, следует ли сохранять поле INCLUDEPICTURE при чтении форматов Microsoft Word. Значение по умолчанию:`ЛОЖЬ` . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Вызывается во время загрузки документа и принимает данные о ходе загрузки. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Позволяет контролировать загрузку внешних ресурсов (изображений, таблиц стилей) при импорте документа из HTML, MHTML. |
| [SupportFontFaceRules](../../aspose.words.loading/htmlloadoptions/supportfontfacerules/) { get; set; } | Возвращает или задает значение, указывающее, следует ли поддерживать правила @font-face и загружать ли объявленные шрифты. Значение по умолчанию:`ЛОЖЬ` . |
| [SupportVml](../../aspose.words.loading/htmlloadoptions/supportvml/) { get; set; } | Возвращает или задает значение, указывающее, следует ли поддерживать изображения VML. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Позволяет использовать временные файлы при чтении документа. По умолчанию это свойство`нулевой` и временные файлы не используются. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Указывает, следует ли обновлять поля с помощью`грязный` атрибут. |
| [UseSystemLcid](../../aspose.words.loading/loadoptions/usesystemlcid/) { get; set; } | Возвращает или задает, следует ли использовать значение LCID, полученное из реестра Windows, для определения полей страницы по умолчанию. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Вызывается во время операции загрузки, когда обнаружена проблема, которая может привести к потере точности данных или форматирования. |
| [WebRequestTimeout](../../aspose.words.loading/htmlloadoptions/webrequesttimeout/) { get; set; } | Количество миллисекунд ожидания до тайм-аута веб-запроса. Значение по умолчанию — 100000 миллисекунд (100 секунд). |

## Методы

| Имя | Описание |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(*object*) | Определяет, равен ли указанный объект по значению текущему объекту. |

## Примеры

Показывает, как поддерживать условные комментарии при загрузке HTML-документа.

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();

// Если значение равно true, то мы учитываем код VML при анализе загруженного документа.
loadOptions.SupportVml = supportVml;

// Этот документ содержит изображение JPEG в тегах "<!--[if gte vml 1]>",
// и другое изображение PNG в тегах "<![if !vml]>".
// Если установить флаг «SupportVml» на «true», то Aspose.Words загрузит JPEG.
// Если мы установим этот флаг на «false», то Aspose.Words загрузит только PNG.
Document doc = new Document(MyDir + "VML conditional.htm", loadOptions);

if (supportVml)
    Assert.AreEqual(ImageType.Jpeg, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
else
    Assert.AreEqual(ImageType.Png, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
```

### Смотрите также

* class [LoadOptions](../loadoptions/)
* пространство имен [Aspose.Words.Loading](../../aspose.words.loading/)
* сборка [Aspose.Words](../../)
