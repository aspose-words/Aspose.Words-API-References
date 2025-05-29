---
title: HtmlSaveOptions.FontResourcesSubsettingSizeThreshold
linktitle: FontResourcesSubsettingSizeThreshold
articleTitle: FontResourcesSubsettingSizeThreshold
second_title: Aspose.Words для .NET
description: Оптимизируйте файлы HTML, MHTML или EPUB с помощью свойства FontResourcesSubsettingSizeThreshold, обеспечивающего эффективное управление ресурсами шрифта. По умолчанию 0.
type: docs
weight: 290
url: /ru/net/aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold/
---
## HtmlSaveOptions.FontResourcesSubsettingSizeThreshold property

Управляет тем, какие ресурсы шрифта требуют поднабора при сохранении в HTML, MHTML или EPUB. Значение по умолчанию:`0` .

```csharp
public int FontResourcesSubsettingSizeThreshold { get; set; }
```

## Примечания

[`ExportFontResources`](../exportfontresources/) позволяет экспортировать шрифты как вспомогательные файлы или как части пакета output . Если в документе используется много шрифтов, особенно с большим количеством глифов, то размер вывода может значительно вырасти . Поднабор шрифтов уменьшает размер экспортируемого ресурса шрифта, отфильтровывая глифы, которые не используются текущим документом.

Подмножество шрифтов работает следующим образом:

* По умолчанию все экспортируемые шрифты имеют подмножества.
* Параметр`FontResourcesSubsettingSizeThreshold` положительное значение указывает Aspose.Words на необходимость выделения подмножества шрифтов, размер файла которых больше указанного значения.
* Установка свойства вMaxValue подавляет поднабор шрифта.

**Важный!**При экспорте ресурсов шрифтов следует учитывать вопросы лицензирования шрифтов. Авторы, желающие использовать определенные шрифты через механизм загружаемых шрифтов, должны всегда тщательно проверять, что их предполагаемое использование находится в рамках лицензии шрифта. Многие коммерческие шрифты в настоящее время не позволяют загружать свои шрифты из Интернета в любой форме. Лицензионные соглашения, охватывающие некоторые шрифты, специально отмечают, что использование через**@шрифт-face** rules в таблицах стилей CSS не допускается. Подмножество шрифтов также может нарушать условия лицензии.

## Примеры

Показывает, как работать с подмножеством шрифтов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Times New Roman";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("Hello world!");

// При сохранении документа в формате HTML мы можем передать объект SaveOptions для настройки поднабора шрифтов.
// Предположим, мы устанавливаем флаг «ExportFontResources» в значение «true», а также указываем имя папки в свойстве «FontsFolder».
// В этом случае операция сохранения создаст эту папку и поместит в нее файл .ttf
// эта папка для каждого шрифта, который использует наш документ.
// Каждый файл .ttf будет содержать весь набор глифов этого шрифта,
// что может привести к созданию очень большого файла, сопровождающего документ.
// Когда мы применяем поднабор к шрифту, его экспортированные необработанные данные будут содержать только те глифы, которые есть в документе
// использование вместо всего набора глифов. Если текст в нашем документе использует только небольшую часть шрифта
// набор глифов, то подмножество значительно сократит размер наших выходных документов.
// Мы можем использовать свойство "FontResourcesSubsettingSizeThreshold" для определения размера файла .ttf в байтах.
 // Если экспортированный шрифт создает файл большего размера, то операция сохранения применит поднабор к этому шрифту.
// Установка порогового значения 0 применяет поднабор ко всем шрифтам,
// и установка его в "int.MaxValue" фактически отключает поднабор.
string fontsFolder = ArtifactsDir + "HtmlSaveOptions.FontSubsetting.Fonts";

HtmlSaveOptions options = new HtmlSaveOptions
{
    ExportFontResources = true,
    FontsFolder = fontsFolder,
    FontResourcesSubsettingSizeThreshold = fontResourcesSubsettingSizeThreshold
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.FontSubsetting.html", options);

string[] fontFileNames = Directory.GetFiles(fontsFolder).Where(s => s.EndsWith(".ttf")).ToArray();

Assert.AreEqual(3, fontFileNames.Length);

foreach (string filename in fontFileNames)
{
    // По умолчанию файлы .ttf для каждого из наших трех шрифтов будут иметь размер более 700 МБ.
    // Подмножество сократит их все до размера менее 30 МБ.
    FileInfo fontFileInfo = new FileInfo(filename);

    Assert.True(fontFileInfo.Length > 700000 || fontFileInfo.Length < 30000);
    Assert.True(Math.Max(fontResourcesSubsettingSizeThreshold, 30000) > new FileInfo(filename).Length);
}
```

### Смотрите также

* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
