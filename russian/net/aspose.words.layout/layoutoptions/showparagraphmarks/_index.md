---
title: LayoutOptions.ShowParagraphMarks
linktitle: ShowParagraphMarks
articleTitle: ShowParagraphMarks
second_title: Aspose.Words для .NET
description: Узнайте, как свойство LayoutOptions ShowParagraphMarks улучшает форматирование текста, переключая видимость знаков абзаца. Улучшите ясность вашего документа сегодня!
type: docs
weight: 90
url: /ru/net/aspose.words.layout/layoutoptions/showparagraphmarks/
---
## LayoutOptions.ShowParagraphMarks property

Возвращает или задает указание того, отображаются ли знаки абзаца. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ShowParagraphMarks { get; set; }
```

## Примеры

Показывает, как отображать знаки абзацев в визуализированном выходном документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Добавьте несколько абзацев, затем включите знаки абзацев, чтобы отображать концы абзацев
// с символом "¶" при рендеринге документа.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

### Смотрите также

* class [LayoutOptions](../)
* пространство имен [Aspose.Words.Layout](../../../aspose.words.layout/)
* сборка [Aspose.Words](../../../)
