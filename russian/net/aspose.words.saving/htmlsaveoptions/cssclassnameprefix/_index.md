---
title: HtmlSaveOptions.CssClassNamePrefix
linktitle: CssClassNamePrefix
articleTitle: CssClassNamePrefix
second_title: Aspose.Words для .NET
description: Откройте для себя свойство HtmlSaveOptions CssClassNamePrefix, позволяющее легко настраивать имена классов CSS с помощью уникального префикса, повышая согласованность вашего веб-дизайна.
type: docs
weight: 30
url: /ru/net/aspose.words.saving/htmlsaveoptions/cssclassnameprefix/
---
## HtmlSaveOptions.CssClassNamePrefix property

Указывает префикс, который добавляется ко всем именам классов CSS. Значением по умолчанию является пустая строка, а сгенерированные имена классов CSS не имеют общего префикса.

```csharp
public string CssClassNamePrefix { get; set; }
```

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentException | Значение не пустое и не является допустимым идентификатором CSS. |

## Примечания

Если это значение не пустое, все классы CSS, сгенерированные Aspose.Words, будут начинаться с указанного префикса . . Это может быть полезно, например, если вы добавляете пользовательский CSS в сгенерированные документы и хотите предотвратить конфликты имен class .

Если значение не равно`нулевой` или пустым, это должен быть действительный идентификатор CSS.

## Примеры

Показывает, как сохранить документ в формате HTML и добавить префикс ко всем именам его классов CSS.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

HtmlSaveOptions saveOptions = new HtmlSaveOptions
{
    CssStyleSheetType = CssStyleSheetType.External,
    CssClassNamePrefix = "myprefix-"
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.CssClassNamePrefix.html", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.CssClassNamePrefix.html");

Assert.True(outDocContents.Contains("<p class=\"myprefix-Header\">"));
Assert.True(outDocContents.Contains("<p class=\"myprefix-Footer\">"));

outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.CssClassNamePrefix.css");

Assert.True(outDocContents.Contains(".myprefix-Footer { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt; -aw-style-name:footer }"));
Assert.True(outDocContents.Contains(".myprefix-Header { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt; -aw-style-name:header }"));
```

### Смотрите также

* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
