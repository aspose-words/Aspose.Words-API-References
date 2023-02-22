---
title: HtmlSaveOptions.FontResourcesSubsettingSizeThreshold
second_title: Справочник по API Aspose.Words для .NET
description: HtmlSaveOptions свойство. Управляет тем какие ресурсы шрифтов нуждаются в подразделении при сохранении в HTML MHTML или EPUB. Значение по умолчанию0 .
type: docs
weight: 300
url: /ru/net/aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold/
---
## HtmlSaveOptions.FontResourcesSubsettingSizeThreshold property

Управляет тем, какие ресурсы шрифтов нуждаются в подразделении при сохранении в HTML, MHTML или EPUB. Значение по умолчанию:`0` .

```csharp
public int FontResourcesSubsettingSizeThreshold { get; set; }
```

### Примечания

[`ExportFontResources`](../exportfontresources/) позволяет экспортировать шрифты как вспомогательные файлы или как части пакета output . Если в документе используется много шрифтов, особенно с большим количеством глифов, то размер вывода может значительно увеличиться . Подмножество шрифтов уменьшает размер экспортируемого ресурса шрифта, отфильтровывая глифы, которые не используются текущим документом.

Подмножество шрифтов работает следующим образом:

* По умолчанию все экспортируемые шрифты являются подмножествами.
* Параметр`FontResourcesSubsettingSizeThreshold`в положительное значение указывает Aspose.Words на подмножество шрифтов, размер файла которых превышает указанное значение.
* Установка свойства наMaxValue подавляет поднабор шрифта.

**Важный!** При экспорте ресурсов шрифтов следует учитывать вопросы лицензирования шрифтов. Авторы, которые хотят использовать определенные шрифты через механизм шрифтов downloadable , должны всегда тщательно проверять, что их предполагаемое использование находится в рамках лицензии на шрифт. Многие коммерческие шрифты в настоящее время не позволяют загружать свои шрифты из Интернета в любой форме. В лицензионных соглашениях, распространяющихся на некоторые шрифты, особо отмечается, что использование через **@шрифт-лицо** rules в таблицах стилей CSS не допускается. Подмножество шрифтов также может нарушать условия лицензии.

### Примеры

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

// Когда мы сохраняем документ в HTML, мы можем передать объект SaveOptions для настройки поднастройки шрифта.
// Допустим, мы установили флаг "ExportFontResources" в "true" и также назвали папку в свойстве "FontsFolder".
// В этом случае операция сохранения создаст эту папку и поместит в нее файл .ttf
// эта папка для каждого шрифта, используемого в нашем документе.
// Каждый файл .ttf будет содержать весь набор глифов этого шрифта,
// что потенциально может привести к созданию очень большого файла, сопровождающего документ.
// Когда мы применяем подмножество к шрифту, его экспортированные необработанные данные будут содержать только те глифы, которые содержит документ
// использование вместо всего набора глифов. Если текст в нашем документе использует только небольшую часть шрифта
// набор глифов, то подмножество значительно уменьшит размер наших выходных документов.
// Мы можем использовать свойство «FontResourcesSubsettingSizeThreshold», чтобы определить размер файла .ttf в байтах.
 // Если экспортированный шрифт создает файл большего размера, чем этот, то операция сохранения применит подмножество к этому шрифту.
// Установка порога 0 применяет подмножество ко всем шрифтам,
// и установка его в "int.MaxValue" эффективно отключает подмножество.
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
    // Подмножество уменьшит их размер до 30 МБ.
    FileInfo fontFileInfo = new FileInfo(filename);

    Assert.True(fontFileInfo.Length > 700000 || fontFileInfo.Length < 30000);
    Assert.True(Math.Max(fontResourcesSubsettingSizeThreshold, 30000) > new FileInfo(filename).Length);
}
```

### Смотрите также

* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../htmlsaveoptions/)
* сборка [Aspose.Words](../../../)


