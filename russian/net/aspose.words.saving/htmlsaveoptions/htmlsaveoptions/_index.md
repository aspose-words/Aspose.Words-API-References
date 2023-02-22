---
title: HtmlSaveOptions.HtmlSaveOptions
second_title: Справочник по API Aspose.Words для .NET
description: HtmlSaveOptions строитель. Инициализирует новый экземпляр этого класса который можно использовать для сохранения документа вHtml формат.
type: docs
weight: 10
url: /ru/net/aspose.words.saving/htmlsaveoptions/htmlsaveoptions/
---
## HtmlSaveOptions() {#constructor}

Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа вHtml формат.

```csharp
public HtmlSaveOptions()
```

### Примеры

Показывает, как использовать определенную кодировку при сохранении документа в формате .epub.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Используйте объект SaveOptions для указания кодировки сохраняемого документа.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// По умолчанию выходной документ .epub будет иметь все свое содержимое в одной HTML-части.
// Критерий разделения позволяет нам разделить документ на несколько частей HTML.
// Мы установим критерии для разделения документа на абзацы заголовков.
// Это полезно для читателей, которые не могут читать файлы HTML, размер которых превышает определенный.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Указываем, что хотим экспортировать свойства документа.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### Смотрите также

* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../htmlsaveoptions/)
* сборка [Aspose.Words](../../../)

---

## HtmlSaveOptions(SaveFormat) {#constructor_1}

Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа вHtml ,Mhtml илиEpub формат.

```csharp
public HtmlSaveOptions(SaveFormat saveFormat)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| saveFormat | SaveFormat | Может бытьHtml ,Mhtml илиEpub. |

### Примеры

Показывает, как сохранить документ в определенной версии HTML.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    HtmlVersion = htmlVersion,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.HtmlVersions.html", options);

// Наши HTML-документы будут иметь незначительные отличия, чтобы быть совместимыми с разными версиями HTML.
string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.HtmlVersions.html");

switch (htmlVersion)
{
    case HtmlVersion.Html5:
        Assert.True(outDocContents.Contains("<a id=\"_Toc76372689\"></a>"));
        Assert.True(outDocContents.Contains("<a id=\"_Toc76372689\"></a>"));
        Assert.True(outDocContents.Contains("<table style=\"-aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
        break;
    case HtmlVersion.Xhtml:
        Assert.True(outDocContents.Contains("<a name=\"_Toc76372689\"></a>"));
        Assert.True(outDocContents.Contains("<ul type=\"disc\" style=\"margin:0pt; padding-left:0pt\">"));
        Assert.True(outDocContents.Contains("<table cellspacing=\"0\" cellpadding=\"0\" style=\"-aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\""));
        break;
}
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../htmlsaveoptions/)
* сборка [Aspose.Words](../../../)


