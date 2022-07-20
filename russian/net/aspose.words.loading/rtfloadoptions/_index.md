---
title: RtfLoadOptions
second_title: Справочник по API Aspose.Words для .NET
description: Позволяет указать дополнительные параметры при загрузкеRtf документ вDocument../aspose.words/document объект.
type: docs
weight: 3510
url: /ru/net/aspose.words.loading/rtfloadoptions/
---
## RtfLoadOptions class

Позволяет указать дополнительные параметры при загрузкеRtf документ в[`Document`](../../aspose.words/document) объект.

```csharp
public class RtfLoadOptions : LoadOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [RtfLoadOptions](rtfloadoptions)() | Инициализирует новый экземпляр этого класса со значениями по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri) { get; set; } | Получает или задает строку, которая будет использоваться для преобразования относительных URI, найденных в документе, в абсолютные URI, когда это необходимо. Может быть нулевой или пустой строкой. Значение по умолчанию — null. |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng) { get; set; } | Получает или задает, следует ли преобразовывать метафайл (Wmf или жеEmf ) изображения вPng формат изображения. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath) { get; set; } | Получает или задает, следует ли преобразовывать фигуры с помощью EquationXML в объекты Office Math. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding) { get; set; } | Получает или задает кодировку, которая будет использоваться для загрузки документа HTML, TXT или CHM, если кодировка не указана внутри документа. Может быть нулевым. Значение по умолчанию — null. |
| [FlatOpcXmlMappingOnly](../../aspose.words.loading/loadoptions/flatopcxmlmappingonly) { get; set; } | Получает или задает значение, определяющее, какие форматы документов разрешено отображать[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping) . Только по умолчаниюFlatOpc формат документа разрешен для сопоставления. |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings) { get; set; } | Позволяет указать настройки шрифта документа. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences) { get; } | Получает языковые настройки, которые будут использоваться при загрузке документа. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat) { get; set; } | Указывает формат загружаемого документа. Значение по умолчанию:Auto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion) { get; set; } | Позволяет указать, что процесс загрузки документа должен соответствовать конкретной версии MS Word. Значение по умолчанию:Word2019 |
| [Password](../../aspose.words.loading/loadoptions/password) { get; set; } | Получает или задает пароль для открытия зашифрованного документа. Может быть нулевым или пустой строкой. Значение по умолчанию — null. |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield) { get; set; } | Получает или задает, следует ли сохранять поле INCLUDEPICTURE при чтении форматов Microsoft Word. Значение по умолчанию — false. |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback) { get; set; } | Вызывается при загрузке документа и принимает данные о ходе загрузки. |
| [RecognizeUtf8Text](../../aspose.words.loading/rtfloadoptions/recognizeutf8text) { get; set; } | Если установлено значение true,CharsetDetectorпопытается обнаружить символы UTF8, они будут сохранены при импорте. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback) { get; set; } | Позволяет управлять загрузкой внешних ресурсов (изображений, таблиц стилей) при импорте документа из HTML, MHTML. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder) { get; set; } | Позволяет использовать временные файлы при чтении документа. По умолчанию это свойство`нулевой` и никакие временные файлы не используются. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields) { get; set; } | Указывает, обновлять ли поля с`грязный` атрибут. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback) { get; set; } | Вызывается во время операции загрузки при обнаружении проблемы, которая может привести к потере точности данных или форматирования. |

### Примеры

Показывает, как обнаруживать символы UTF-8 при загрузке документа RTF.

```csharp
// Создайте объект «RtfLoadOptions», чтобы изменить способ загрузки RTF-документа.
RtfLoadOptions loadOptions = new RtfLoadOptions();

// Установите для свойства "RecognizeUtf8Text" значение "false", чтобы предположить, что документ использует кодировку ISO 8859-1
// и загружает каждый символ в документе.
// Установите для свойства "RecognizeUtf8Text" значение "true", чтобы анализировать любые символы переменной длины, которые могут встречаться в тексте.
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

* class [LoadOptions](../loadoptions)
* пространство имен [Aspose.Words.Loading](../../aspose.words.loading)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
