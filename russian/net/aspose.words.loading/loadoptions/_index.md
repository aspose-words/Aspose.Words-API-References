---
title: Class LoadOptions
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Loading.LoadOptions сорт. Позволяет указать дополнительные параметры например пароль или базовый URI при загрузке документа вDocument объект.
type: docs
weight: 3460
url: /ru/net/aspose.words.loading/loadoptions/
---
## LoadOptions class

Позволяет указать дополнительные параметры (например, пароль или базовый URI) при загрузке документа в[`Document`](../../aspose.words/document/) объект.

```csharp
public class LoadOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [LoadOptions](loadoptions/#constructor)() | Инициализирует новый экземпляр этого класса со значениями по умолчанию. |
| [LoadOptions](loadoptions/#constructor_2)(string) | Ярлык для инициализации нового экземпляра этого класса с указанным паролем для загрузки зашифрованного документа. |
| [LoadOptions](loadoptions/#constructor_1)(LoadFormat, string, string) | Ярлык для инициализации нового экземпляра этого класса со свойствами, установленными на указанные значения. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Получает или задает строку, которая будет использоваться для преобразования относительных URI, найденных в документе, в абсолютные URI, когда это необходимо. Может быть нулевой или пустой строкой. Значение по умолчанию — null. |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Получает или задает, следует ли преобразовывать метафайл (Wmf или жеEmf ) изображения вPng формат изображения. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Получает или задает, следует ли преобразовывать фигуры с помощью EquationXML в объекты Office Math. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Получает или задает кодировку, которая будет использоваться для загрузки документа HTML, TXT или CHM, если кодировка не указана внутри документа. Может быть нулевым. Значение по умолчанию — null. |
| [FlatOpcXmlMappingOnly](../../aspose.words.loading/loadoptions/flatopcxmlmappingonly/) { get; set; } | Получает или задает значение, определяющее, какие форматы документов разрешено отображать[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Только по умолчаниюFlatOpc формат документа разрешен для сопоставления. |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Позволяет указать настройки шрифта документа. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Получает языковые настройки, которые будут использоваться при загрузке документа. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Указывает формат загружаемого документа. Значение по умолчанию:Auto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Позволяет указать, что процесс загрузки документа должен соответствовать конкретной версии MS Word. Значение по умолчанию:Word2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Получает или задает пароль для открытия зашифрованного документа. Может быть нулевым или пустой строкой. Значение по умолчанию — null. |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Получает или задает, следует ли сохранять поле INCLUDEPICTURE при чтении форматов Microsoft Word. Значение по умолчанию — false. |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Вызывается при загрузке документа и принимает данные о ходе загрузки. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Позволяет управлять загрузкой внешних ресурсов (изображений, таблиц стилей) при импорте документа из HTML, MHTML. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Позволяет использовать временные файлы при чтении документа. По умолчанию это свойство`нулевой` и никакие временные файлы не используются. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Указывает, обновлять ли поля с`грязный` атрибут. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Вызывается во время операции загрузки при обнаружении проблемы, которая может привести к потере точности данных или форматирования. |

### Примеры

Показывает, как загрузить зашифрованный документ Microsoft Word.

```csharp
Document doc;

// Aspose.Words выдает исключение, если мы пытаемся открыть зашифрованный документ без пароля.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// При загрузке такого документа пароль передается конструктору документа с помощью объекта LoadOptions.
LoadOptions options = new LoadOptions("docPassword");

// Есть два способа загрузки зашифрованного документа с помощью объекта LoadOptions.
// 1 - Загрузить документ из локальной файловой системы по имени файла:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - Загрузить документ из потока:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
```

### Смотрите также

* пространство имен [Aspose.Words.Loading](../../aspose.words.loading/)
* сборка [Aspose.Words](../../)


