---
title: Document.LayoutOptions
second_title: Справочник по API Aspose.Words для .NET
description: Document свойство. Получает МакетОпции объект представляющий параметры для управления процессом компоновки этого документа.
type: docs
weight: 230
url: /ru/net/aspose.words/document/layoutoptions/
---
## Document.LayoutOptions property

Получает **МакетОпции** объект, представляющий параметры для управления процессом компоновки этого документа.

```csharp
public LayoutOptions LayoutOptions { get; }
```

### Примеры

Показывает, как скрыть текст в визуализируемом выходном документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Вставляем скрытый текст, затем указываем, хотим ли мы исключить его из визуализируемого документа.
builder.Writeln("This text is not hidden.");
builder.Font.Hidden = true;
builder.Writeln("This text is hidden.");

doc.LayoutOptions.ShowHiddenText = showHiddenText;

doc.Save(ArtifactsDir + "Document.LayoutOptionsHiddenText.pdf");
```

Показывает, как отображать метки абзаца в визуализируемом выходном документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Добавьте несколько абзацев, затем включите метки абзаца, чтобы показать концы абзацев
// с символом пилкроу (¶) при отображении документа.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

Показывает, как изменить внешний вид редакций в подготовленном к просмотру выходном документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте ревизию, затем измените цвет всех ревизий на зеленый.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Удаляем полосу, которая появляется слева от каждой исправленной строки.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;

doc.Save(ArtifactsDir + "Document.LayoutOptionsRevisions.pdf");
```

### Смотрите также

* class [LayoutOptions](../../../aspose.words.layout/layoutoptions/)
* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)


