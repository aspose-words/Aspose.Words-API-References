---
title: LoadOptions Class
linktitle: LoadOptions
articleTitle: LoadOptions
second_title: Aspose.Words для .NET
description: Откройте для себя Aspose.Words.LoadOptions для улучшенной загрузки документов. Устанавливайте пароли и базовые URI без усилий для бесшовной интеграции и безопасности.
type: docs
weight: 4110
url: /ru/net/aspose.words.loading/loadoptions/
---
## LoadOptions class

Позволяет указать дополнительные параметры (например, пароль или базовый URI) при загрузке документа в[`Document`](../../aspose.words/document/) объект.

Чтобы узнать больше, посетите[Укажите параметры загрузки](https://docs.aspose.com/words/net/specify-load-options/) документальная статья.

```csharp
public class LoadOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [LoadOptions](loadoptions/#constructor)() | Инициализирует новый экземпляр этого класса со значениями по умолчанию. |
| [LoadOptions](loadoptions/#constructor_2)(*string*) | Ярлык для инициализации нового экземпляра этого класса с указанным паролем для загрузки зашифрованного документа. |
| [LoadOptions](loadoptions/#constructor_1)(*[LoadFormat](../../aspose.words/loadformat/), string, string*) | Ярлык для инициализации нового экземпляра этого класса со свойствами, установленными на указанные значения. |

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

Показывает, как загрузить зашифрованный документ Microsoft Word.

```csharp
Document doc;

// Aspose.Words выдает исключение, если мы пытаемся открыть зашифрованный документ без его пароля.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// При загрузке такого документа пароль передается конструктору документа с помощью объекта LoadOptions.
LoadOptions options = new LoadOptions("docPassword");

// Существует два способа загрузки зашифрованного документа с помощью объекта LoadOptions.
// 1 - Загрузить документ из локальной файловой системы по имени файла:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - Загрузить документ из потока:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
}
```

### Смотрите также

* пространство имен [Aspose.Words.Loading](../../aspose.words.loading/)
* сборка [Aspose.Words](../../)
