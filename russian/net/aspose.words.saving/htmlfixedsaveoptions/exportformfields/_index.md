---
title: HtmlFixedSaveOptions.ExportFormFields
linktitle: ExportFormFields
articleTitle: ExportFormFields
second_title: Aspose.Words для .NET
description: HtmlFixedSaveOptions ExportFormFields свойство. Получает или задает указание того экспортируются ли поля формы как элементы интерактивного как тег ввода а не преобразуются ли они в текст или графику на С#.
type: docs
weight: 80
url: /ru/net/aspose.words.saving/htmlfixedsaveoptions/exportformfields/
---
## HtmlFixedSaveOptions.ExportFormFields property

Получает или задает указание того, экспортируются ли поля формы как элементы интерактивного (как тег ввода), а не преобразуются ли они в текст или графику.

```csharp
public bool ExportFormFields { get; set; }
```

## Примеры

Показывает, как экспортировать поля формы в Html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertCheckBox("CheckBox", false, 15);

// Когда мы экспортируем документ с полями формы в .html,
// существует два способа, которыми Aspose.Words может экспортировать поля формы.
// Установка флага «ExportFormFields» в значение «true» экспортирует их как интерактивные объекты.
// Установка этого флага в значение «false» будет отображать поля формы в виде обычного текста.
// Это заморозит их текущие значения и не позволит читателю нашего HTML-документа
// от возможности взаимодействовать с ними.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportFormFields = exportFormFields
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportFormFields.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportFormFields.html");

if (exportFormFields)
{
    Assert.True(Regex.Match(outDocContents,
        "<a name=\"CheckBox\" style=\"left:0pt; top:0pt;\"></a>" +
        "<input style=\"position:absolute; left:0pt; top:0pt;\" type=\"checkbox\" name=\"CheckBox\" />").Success);
}
else
{
    Assert.True(Regex.Match(outDocContents, 
        "<a name=\"CheckBox\" style=\"left:0pt; top:0pt;\"></a>" +
        "<div class=\"awdiv\" style=\"left:0.8pt; top:0.8pt; width:14.25pt; height:14.25pt; border:solid 0.75pt #000000;\"").Success);
}
```

### Смотрите также

* class [HtmlFixedSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
