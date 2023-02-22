---
title: HtmlSaveOptions.CssClassNamePrefix
second_title: Справочник по API Aspose.Words для .NET
description: HtmlSaveOptions свойство. Указывает префикс который добавляется ко всем именам классов CSS. Значение по умолчанию  пустая строка а сгенерированные имена классов CSS не имеют общего префикса.
type: docs
weight: 30
url: /ru/net/aspose.words.saving/htmlsaveoptions/cssclassnameprefix/
---
## HtmlSaveOptions.CssClassNamePrefix property

Указывает префикс, который добавляется ко всем именам классов CSS. Значение по умолчанию — пустая строка, а сгенерированные имена классов CSS не имеют общего префикса.

```csharp
public string CssClassNamePrefix { get; set; }
```

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentException | Значение не является пустым и не является допустимым идентификатором CSS. |

### Примечания

Если это значение не пустое, все классы CSS, сгенерированные Aspose.Words, будут начинаться с указанного префикса. Это может быть полезно, например, если вы добавляете пользовательский CSS в сгенерированные документы и хотите предотвратить конфликты имен class .

Если значение не`нулевой` или пустым, это должен быть действительный идентификатор CSS.

### Примеры

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

Assert.True(outDocContents.Contains(".myprefix-Footer { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt }\r\n" +
                                    ".myprefix-Header { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt }\r\n"));
```

### Смотрите также

* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../htmlsaveoptions/)
* сборка [Aspose.Words](../../../)


