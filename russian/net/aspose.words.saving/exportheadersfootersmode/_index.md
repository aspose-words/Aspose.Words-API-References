---
title: Enum ExportHeadersFootersMode
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Saving.ExportHeadersFootersMode перечисление. Указывает как верхние и нижние колонтитулы экспортируются в HTML MHTML или EPUB.
type: docs
weight: 4740
url: /ru/net/aspose.words.saving/exportheadersfootersmode/
---
## ExportHeadersFootersMode enumeration

Указывает, как верхние и нижние колонтитулы экспортируются в HTML, MHTML или EPUB.

```csharp
public enum ExportHeadersFootersMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Верхние и нижние колонтитулы не экспортируются. |
| PerSection | `1` | Основные верхние и нижние колонтитулы экспортируются в начале и в конце каждого раздела. |
| FirstSectionHeaderLastSectionFooter | `2` | Основной заголовок первого раздела экспортируется в начало документа, а основной нижний колонтитул — в конец. |
| FirstPageHeaderFooterPerSection | `3` | Верхний и нижний колонтитулы первой страницы экспортируются в начале и в конце каждого раздела. |

### Примеры

Показывает, как опускать верхние и нижние колонтитулы при сохранении документа в формате HTML.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Этот документ содержит верхние и нижние колонтитулы. Мы можем получить к ним доступ через коллекцию «HeadersFooters».
Assert.AreEqual("First header", doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderFirst].GetText().Trim());

// Такие форматы, как .html, не разбивают документ на страницы, поэтому верхние и нижние колонтитулы не будут работать одинаково
// они будут, когда мы откроем документ в формате .docx с помощью Microsoft Word.
// Если мы преобразуем документ с верхними/нижними колонтитулами в html, преобразование ассимилирует верхние/нижние колонтитулы в основной текст.
// Мы можем использовать объект SaveOptions, чтобы опустить верхние/нижние колонтитулы при преобразовании в html.
HtmlSaveOptions saveOptions =
    new HtmlSaveOptions(SaveFormat.Html) { ExportHeadersFootersMode = ExportHeadersFootersMode.None };

doc.Save(ArtifactsDir + "HeaderFooter.ExportMode.html", saveOptions);

// Открываем наш сохраненный документ и проверяем, что он не содержит текста заголовка
doc = new Document(ArtifactsDir + "HeaderFooter.ExportMode.html");

Assert.IsFalse(doc.Range.Text.Contains("First header"));
```

### Смотрите также

* property [ExportHeadersFootersMode](../htmlsaveoptions/exportheadersfootersmode/)
* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)


