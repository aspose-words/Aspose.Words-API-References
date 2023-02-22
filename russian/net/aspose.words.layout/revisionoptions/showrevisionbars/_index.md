---
title: RevisionOptions.ShowRevisionBars
second_title: Справочник по API Aspose.Words для .NET
description: RevisionOptions свойство. Позволяет указать следует ли отображать полосы изменений рядом со строками содержащими исправленное содержимое. Значение по умолчанию  True.
type: docs
weight: 180
url: /ru/net/aspose.words.layout/revisionoptions/showrevisionbars/
---
## RevisionOptions.ShowRevisionBars property

Позволяет указать, следует ли отображать полосы изменений рядом со строками, содержащими исправленное содержимое. Значение по умолчанию — True.

```csharp
public bool ShowRevisionBars { get; set; }
```

### Примеры

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

* class [RevisionOptions](../)
* пространство имен [Aspose.Words.Layout](../../revisionoptions/)
* сборка [Aspose.Words](../../../)


