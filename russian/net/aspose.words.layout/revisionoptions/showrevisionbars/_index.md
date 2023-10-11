---
title: RevisionOptions.ShowRevisionBars
second_title: Справочник по API Aspose.Words для .NET
description: RevisionOptions свойство. Позволяет указать должны ли полосы изменений отображаться рядом со строками содержащими измененный контент. Значение по умолчаниюистинный .
type: docs
weight: 180
url: /ru/net/aspose.words.layout/revisionoptions/showrevisionbars/
---
## RevisionOptions.ShowRevisionBars property

Позволяет указать, должны ли полосы изменений отображаться рядом со строками, содержащими измененный контент. Значение по умолчанию:`истинный` .

```csharp
public bool ShowRevisionBars { get; set; }
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

* class [RevisionOptions](../)
* пространство имен [Aspose.Words.Layout](../../revisionoptions/)
* сборка [Aspose.Words](../../../)


