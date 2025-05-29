---
title: TxtLoadOptions Class
linktitle: TxtLoadOptions
articleTitle: TxtLoadOptions
second_title: Aspose.Words для .NET
description: Откройте для себя Aspose.Words.TxtLoadOptions для улучшенной загрузки текстовых документов. Настройте свой объект Document с помощью гибких параметров для оптимальной производительности.
type: docs
weight: 4190
url: /ru/net/aspose.words.loading/txtloadoptions/
---
## TxtLoadOptions class

Позволяет указать дополнительные параметры при загрузкеText документ в[`Document`](../../aspose.words/document/) объект.

Чтобы узнать больше, посетите[Укажите параметры загрузки](https://docs.aspose.com/words/net/specify-load-options/) документальная статья.

```csharp
public class TxtLoadOptions : LoadOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [TxtLoadOptions](txtloadoptions/)() | Инициализирует новый экземпляр этого класса со значениями по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [AutoNumberingDetection](../../aspose.words.loading/txtloadoptions/autonumberingdetection/) { get; set; } | Возвращает или задает логическое значение, указывающее, будет ли выполняться автоматическое определение нумерации при загрузке документа. Значение по умолчанию:`истинный` . |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Возвращает или задает строку, которая будет использоваться для преобразования относительных URI, найденных в документе, в абсолютные URI при необходимости. Может быть`нулевой` или пустая строка. По умолчанию`нулевой` . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Возвращает или задает, следует ли преобразовывать метафайл (Wmf илиEmf ) изображения вPngформат изображения. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Возвращает или задает, следует ли преобразовывать фигуры с EquationXML в объекты Office Math. |
| [DetectHyperlinks](../../aspose.words.loading/txtloadoptions/detecthyperlinks/) { get; set; } | Указывает, следует ли обнаруживать гиперссылки в тексте. Значение по умолчанию:`ЛОЖЬ` . |
| [DetectNumberingWithWhitespaces](../../aspose.words.loading/txtloadoptions/detectnumberingwithwhitespaces/) { get; set; } | Позволяет указать, как распознаются элементы нумерованного списка при импорте документа из обычного текстового формата. Значение по умолчанию:`истинный`. |
| [DocumentDirection](../../aspose.words.loading/txtloadoptions/documentdirection/) { get; set; } | Возвращает или задает направление документа. Значение по умолчанию:LeftToRight . |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Возвращает или задает кодировку, которая будет использоваться для загрузки документа HTML, TXT или CHM, если кодировка не указана внутри документа. Может быть`нулевой` . По умолчанию`нулевой` . |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Позволяет указать настройки шрифта документа. |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | Указывает, следует ли игнорировать данные OLE. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Получает языковые настройки, которые будут использоваться при загрузке документа. |
| [LeadingSpacesOptions](../../aspose.words.loading/txtloadoptions/leadingspacesoptions/) { get; set; } | Возвращает или задает предпочтительный вариант обработки начального пробела. Значение по умолчанию:ConvertToIndent . |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Указывает формат документа для загрузки. Значение по умолчанию:Auto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Позволяет указать, что процесс загрузки документа должен соответствовать определенной версии MS Word. Значение по умолчанию:Word2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Возвращает или задает пароль для открытия зашифрованного документа. Может быть`нулевой` или пустая строка. По умолчанию`нулевой` . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Возвращает или задает, следует ли сохранять поле INCLUDEPICTURE при чтении форматов Microsoft Word. Значение по умолчанию:`ЛОЖЬ` . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Вызывается во время загрузки документа и принимает данные о ходе загрузки. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Позволяет контролировать загрузку внешних ресурсов (изображений, таблиц стилей) при импорте документа из HTML, MHTML. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Позволяет использовать временные файлы при чтении документа. По умолчанию это свойство`нулевой` и временные файлы не используются. |
| [TrailingSpacesOptions](../../aspose.words.loading/txtloadoptions/trailingspacesoptions/) { get; set; } | Возвращает или задает предпочтительный параметр обработки завершающего пробела. Значение по умолчанию:Trim . |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Указывает, следует ли обновлять поля с помощью`грязный` атрибут. |
| [UseSystemLcid](../../aspose.words.loading/loadoptions/usesystemlcid/) { get; set; } | Возвращает или задает, следует ли использовать значение LCID, полученное из реестра Windows, для определения полей страницы по умолчанию. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Вызывается во время операции загрузки, когда обнаружена проблема, которая может привести к потере точности данных или форматирования. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(*object*) | Определяет, равен ли указанный объект по значению текущему объекту. |

## Примеры

Показывает, как читать и отображать гиперссылки.

```csharp
const string inputText = "Some links in TXT:\n" +
        "https://www.aspose.com/\n" +
        "https://docs.aspose.com/words/net/\n";

using (Stream stream = new MemoryStream())
{
    byte[] buf = Encoding.ASCII.GetBytes(inputText);
    stream.Write(buf, 0, buf.Length);

    // Загрузить документ с гиперссылками.
    Document doc = new Document(stream, new TxtLoadOptions() { DetectHyperlinks = true });

    // Печать текста гиперссылки.
    foreach (Field field in doc.Range.Fields)
        Console.WriteLine(field.Result);

    Assert.AreEqual(doc.Range.Fields[0].Result.Trim(), "https://www.aspose.com/");
    Assert.AreEqual(doc.Range.Fields[1].Result.Trim(), "https://docs.aspose.com/words/net/");
}
```

### Смотрите также

* class [LoadOptions](../loadoptions/)
* пространство имен [Aspose.Words.Loading](../../aspose.words.loading/)
* сборка [Aspose.Words](../../)
