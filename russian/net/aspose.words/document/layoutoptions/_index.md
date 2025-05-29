---
title: Document.LayoutOptions
linktitle: LayoutOptions
articleTitle: LayoutOptions
second_title: Aspose.Words для .NET
description: Изучите свойство Document LayoutOptions, чтобы эффективно управлять макетом документа. Разблокируйте гибкие параметры дизайна для оптимальной презентации.
type: docs
weight: 260
url: /ru/net/aspose.words/document/layoutoptions/
---
## Document.LayoutOptions property

Получает[`LayoutOptions`](../../../aspose.words.layout/layoutoptions/) объект, представляющий параметры управления процессом макета этого документа.

```csharp
public LayoutOptions LayoutOptions { get; }
```

## Примеры

Показывает, как скрыть текст в визуализированном выходном документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Вставляем скрытый текст, затем указываем, хотим ли мы исключить его из отображаемого документа.
builder.Writeln("This text is not hidden.");
builder.Font.Hidden = true;
builder.Writeln("This text is hidden.");

doc.LayoutOptions.ShowHiddenText = showHiddenText;

doc.Save(ArtifactsDir + "Document.LayoutOptionsHiddenText.pdf");
```

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

Показывает, как изменить внешний вид изменений в визуализированном выходном документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте ревизию, затем измените цвет всех ревизий на зеленый.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Удалить полосу, которая появляется слева от каждой измененной строки.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;
doc.LayoutOptions.RevisionOptions.RevisionBarsPosition = HorizontalAlignment.Right;

doc.Save(ArtifactsDir + "Revision.LayoutOptionsRevisions.pdf");
```

### Смотрите также

* class [LayoutOptions](../../../aspose.words.layout/layoutoptions/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
