---
title: LayoutOptions.RevisionOptions
second_title: Справочник по API Aspose.Words для .NET
description: LayoutOptions свойство. Получает параметры версии.
type: docs
weight: 70
url: /ru/net/aspose.words.layout/layoutoptions/revisionoptions/
---
## LayoutOptions.RevisionOptions property

Получает параметры версии.

```csharp
public RevisionOptions RevisionOptions { get; }
```

### Примеры

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

* class [RevisionOptions](../../revisionoptions/)
* class [LayoutOptions](../)
* пространство имен [Aspose.Words.Layout](../../layoutoptions/)
* сборка [Aspose.Words](../../../)


