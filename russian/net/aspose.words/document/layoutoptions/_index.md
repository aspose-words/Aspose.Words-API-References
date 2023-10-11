---
title: Document.LayoutOptions
second_title: Справочник по API Aspose.Words для .NET
description: Document свойство. ПолучаетLayoutOptions объект представляющий параметры управления процессом макетирования этого документа.
type: docs
weight: 250
url: /ru/net/aspose.words/document/layoutoptions/
---
## Document.LayoutOptions property

Получает[`LayoutOptions`](../../../aspose.words.layout/layoutoptions/) объект, представляющий параметры управления процессом макетирования этого документа.

```csharp
public LayoutOptions LayoutOptions { get; }
```

### Примеры

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

Показывает, как отображать знаки абзаца в готовом к просмотру выходном документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Добавляем несколько абзацев, затем включаем знаки абзацев, чтобы показывать концы абзацев
// с символом подставки (¶) при рендеринге документа.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

Показывает, как изменить внешний вид редакций в готовом к просмотру выходном документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем ревизию, затем меняем цвет всех ревизий на зеленый.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Удалить полосу, которая появляется слева от каждой измененной строки.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;

doc.Save(ArtifactsDir + "Document.LayoutOptionsRevisions.pdf");
```

### Смотрите также

* class [LayoutOptions](../../../aspose.words.layout/layoutoptions/)
* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)


