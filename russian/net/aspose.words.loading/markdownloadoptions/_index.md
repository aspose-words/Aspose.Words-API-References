---
title: MarkdownLoadOptions Class
linktitle: MarkdownLoadOptions
articleTitle: MarkdownLoadOptions
second_title: Aspose.Words для .NET
description: Откройте для себя Aspose.Words.MarkdownLoadOptions, чтобы улучшить процесс загрузки документов Markdown. Настройте параметры для бесшовной интеграции в ваши проекты.
type: docs
weight: 4120
url: /ru/net/aspose.words.loading/markdownloadoptions/
---
## MarkdownLoadOptions class

Позволяет указать дополнительные параметры при загрузкеMarkdown документ в[`Document`](../../aspose.words/document/) объект.

```csharp
public class MarkdownLoadOptions : LoadOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [MarkdownLoadOptions](markdownloadoptions/)() | Инициализирует новый экземпляр`MarkdownLoadOptions` класс. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Возвращает или задает строку, которая будет использоваться для преобразования относительных URI, найденных в документе, в абсолютные URI при необходимости. Может быть`нулевой` или пустая строка. По умолчанию`нулевой` . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Возвращает или задает, следует ли преобразовывать метафайл (Wmf илиEmf ) изображения вPngформат изображения. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Возвращает или задает, следует ли преобразовывать фигуры с EquationXML в объекты Office Math. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Возвращает или задает кодировку, которая будет использоваться для загрузки документа HTML, TXT или CHM, если кодировка не указана внутри документа. Может быть`нулевой` . По умолчанию`нулевой` . |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Позволяет указать настройки шрифта документа. |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | Указывает, следует ли игнорировать данные OLE. |
| [ImportUnderlineFormatting](../../aspose.words.loading/markdownloadoptions/importunderlineformatting/) { get; set; } | Возвращает или задает логическое значение, указывающее, следует ли распознавать последовательность из двух символов плюс "++" как подчеркивание форматирования текста. Значение по умолчанию:`ЛОЖЬ` . |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Получает языковые настройки, которые будут использоваться при загрузке документа. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Указывает формат документа для загрузки. Значение по умолчанию:Auto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Позволяет указать, что процесс загрузки документа должен соответствовать определенной версии MS Word. Значение по умолчанию:Word2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Возвращает или задает пароль для открытия зашифрованного документа. Может быть`нулевой` или пустая строка. По умолчанию`нулевой` . |
| [PreserveEmptyLines](../../aspose.words.loading/markdownloadoptions/preserveemptylines/) { get; set; } | Возвращает или задает логическое значение, указывающее, следует ли сохранять пустые строки при загрузкеMarkdown document. Значение по умолчанию:`ЛОЖЬ` . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Возвращает или задает, следует ли сохранять поле INCLUDEPICTURE при чтении форматов Microsoft Word. Значение по умолчанию:`ЛОЖЬ` . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Вызывается во время загрузки документа и принимает данные о ходе загрузки. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Позволяет контролировать загрузку внешних ресурсов (изображений, таблиц стилей) при импорте документа из HTML, MHTML. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Позволяет использовать временные файлы при чтении документа. По умолчанию это свойство`нулевой` и временные файлы не используются. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Указывает, следует ли обновлять поля с помощью`грязный` атрибут. |
| [UseSystemLcid](../../aspose.words.loading/loadoptions/usesystemlcid/) { get; set; } | Возвращает или задает, следует ли использовать значение LCID, полученное из реестра Windows, для определения полей страницы по умолчанию. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Вызывается во время операции загрузки, когда обнаружена проблема, которая может привести к потере точности данных или форматирования. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(*object*) | Определяет, равен ли указанный объект по значению текущему объекту. |

## Примеры

Показывает, как сохранить пустую строку при загрузке документа.

```csharp
string mdText = $"{Environment.NewLine}Line1{Environment.NewLine}{Environment.NewLine}Line2{Environment.NewLine}{Environment.NewLine}";
using (MemoryStream stream = new MemoryStream(Encoding.UTF8.GetBytes(mdText)))
{
    MarkdownLoadOptions loadOptions = new MarkdownLoadOptions() { PreserveEmptyLines = true };
    Document doc = new Document(stream, loadOptions);

    Assert.AreEqual("\rLine1\r\rLine2\r\f", doc.GetText());
}
```

### Смотрите также

* class [LoadOptions](../loadoptions/)
* пространство имен [Aspose.Words.Loading](../../aspose.words.loading/)
* сборка [Aspose.Words](../../)
