---
title: HtmlSaveOptions.ExportLanguageInformation
linktitle: ExportLanguageInformation
articleTitle: ExportLanguageInformation
second_title: Aspose.Words для .NET
description: HtmlSaveOptions ExportLanguageInformation свойство. Указывает экспортируется ли языковая информация в HTML MHTML или EPUB. Значение по умолчаниюЛОЖЬ  на С#.
type: docs
weight: 180
url: /ru/net/aspose.words.saving/htmlsaveoptions/exportlanguageinformation/
---
## HtmlSaveOptions.ExportLanguageInformation property

Указывает, экспортируется ли языковая информация в HTML, MHTML или EPUB. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ExportLanguageInformation { get; set; }
```

## Примечания

Когда для этого свойства установлено значение`истинный` Выходы Aspose.Words**язык** Атрибут HTML в элементах document , определяющих язык. Это может быть необходимо для сохранения семантики, связанной с языком.

## Примеры

Показывает, как сохранить информацию о языке при сохранении в .html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Используйте конструктор для написания текста, форматируя его в разных локалях.
builder.Font.LocaleId = new CultureInfo("en-US").LCID;
builder.Writeln("Hello world!");

builder.Font.LocaleId = new CultureInfo("en-GB").LCID;
builder.Writeln("Hello again!");

builder.Font.LocaleId = new CultureInfo("ru-RU").LCID;
builder.Write("Привет, мир!");

// При сохранении документа в HTML мы можем передать объект SaveOptions
// чтобы сохранить или удалить локаль каждого форматированного текста.
// Если мы установим флаг «ExportLanguageInformation» в значение «true»,
// выходной HTML-документ будет содержать локали в атрибутах "lang" <span> теги.
// Если мы установим флаг «ExportLanguageInformation» в значение «false»,
// текст выходного HTML-документа не будет содержать никакой информации о локали.
HtmlSaveOptions options = new HtmlSaveOptions
{
    ExportLanguageInformation = exportLanguageInformation,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportLanguageInformation.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportLanguageInformation.html");

if (exportLanguageInformation)
{
    Assert.True(outDocContents.Contains("<span>Hello world!</span>"));
    Assert.True(outDocContents.Contains("<span lang=\"en-GB\">Hello again!</span>"));
    Assert.True(outDocContents.Contains("<span lang=\"ru-RU\">Привет, мир!</span>"));
}
else
{
    Assert.True(outDocContents.Contains("<span>Hello world!</span>"));
    Assert.True(outDocContents.Contains("<span>Hello again!</span>"));
    Assert.True(outDocContents.Contains("<span>Привет, мир!</span>"));
}
```

### Смотрите также

* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
