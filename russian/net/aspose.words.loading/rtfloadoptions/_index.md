---
title: RtfLoadOptions Class
linktitle: RtfLoadOptions
articleTitle: RtfLoadOptions
second_title: Aspose.Words для .NET
description: Откройте для себя Aspose.Words.RtfLoadOptions, чтобы улучшить загрузку документов RTF с помощью настраиваемых параметров для бесшовной интеграции в ваши проекты.
type: docs
weight: 4170
url: /ru/net/aspose.words.loading/rtfloadoptions/
---
## RtfLoadOptions class

Позволяет указать дополнительные параметры при загрузкеRtf документ в[`Document`](../../aspose.words/document/) объект.

Чтобы узнать больше, посетите[Укажите параметры загрузки](https://docs.aspose.com/words/net/specify-load-options/) документальная статья.

```csharp
public class RtfLoadOptions : LoadOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [RtfLoadOptions](rtfloadoptions/)() | Инициализирует новый экземпляр этого класса со значениями по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Возвращает или задает строку, которая будет использоваться для преобразования относительных URI, найденных в документе, в абсолютные URI при необходимости. Может быть`нулевой` или пустая строка. По умолчанию`нулевой` . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Возвращает или задает, следует ли преобразовывать метафайл (Wmf илиEmf ) изображения вPngформат изображения. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Возвращает или задает, следует ли преобразовывать фигуры с EquationXML в объекты Office Math. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Возвращает или задает кодировку, которая будет использоваться для загрузки документа HTML, TXT или CHM, если кодировка не указана внутри документа. Может быть`нулевой` . По умолчанию`нулевой` . |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Позволяет указать настройки шрифта документа. |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | Указывает, следует ли игнорировать данные OLE. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Получает языковые настройки, которые будут использоваться при загрузке документа. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Указывает формат документа для загрузки. Значение по умолчанию:Auto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Позволяет указать, что процесс загрузки документа должен соответствовать определенной версии MS Word. Значение по умолчанию:Word2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Возвращает или задает пароль для открытия зашифрованного документа. Может быть`нулевой` или пустая строка. По умолчанию`нулевой` . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Возвращает или задает, следует ли сохранять поле INCLUDEPICTURE при чтении форматов Microsoft Word. Значение по умолчанию:`ЛОЖЬ` . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Вызывается во время загрузки документа и принимает данные о ходе загрузки. |
| [RecognizeUtf8Text](../../aspose.words.loading/rtfloadoptions/recognizeutf8text/) { get; set; } | При установке на`истинный` , попытается обнаружить символы UTF8, они будут сохранены во время импорта. |
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

Показывает, как обнаружить символы UTF-8 при загрузке документа RTF.

```csharp
// Создаем объект «RtfLoadOptions» для изменения способа загрузки документа RTF.
RtfLoadOptions loadOptions = new RtfLoadOptions();

// Установите свойство "RecognizeUtf8Text" в значение "false", чтобы предположить, что документ использует кодировку ISO 8859-1
// и загружает каждый символ в документе.
// Установите свойство «RecognizeUtf8Text» в значение «true», чтобы анализировать любые символы переменной длины, которые могут встречаться в тексте.
loadOptions.RecognizeUtf8Text = recognizeUtf8Text;

Document doc = new Document(MyDir + "UTF-8 characters.rtf", loadOptions);

Assert.AreEqual(
    recognizeUtf8Text
        ? "“John Doe´s list of currency symbols”™\r" +
          "€, ¢, £, ¥, ¤"
        : "â€œJohn DoeÂ´s list of currency symbolsâ€\u009dâ„¢\r" +
          "â‚¬, Â¢, Â£, Â¥, Â¤",
    doc.FirstSection.Body.GetText().Trim());
```

### Смотрите также

* class [LoadOptions](../loadoptions/)
* пространство имен [Aspose.Words.Loading](../../aspose.words.loading/)
* сборка [Aspose.Words](../../)
