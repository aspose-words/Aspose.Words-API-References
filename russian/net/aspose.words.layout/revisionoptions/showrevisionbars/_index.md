---
title: RevisionOptions.ShowRevisionBars
linktitle: ShowRevisionBars
articleTitle: ShowRevisionBars
second_title: Aspose.Words для .NET
description: Узнайте, как свойство ShowRevisionBars в RevisionOptions повышает ясность документа, отображая полосы исправлений для отредактированного содержимого. По умолчанию — true.
type: docs
weight: 200
url: /ru/net/aspose.words.layout/revisionoptions/showrevisionbars/
---
## RevisionOptions.ShowRevisionBars property

Позволяет указать, следует ли отображать полосы исправлений рядом со строками, содержащими измененное содержимое. Значение по умолчанию:`истинный` .

```csharp
public bool ShowRevisionBars { get; set; }
```

## Примеры

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

* class [RevisionOptions](../)
* пространство имен [Aspose.Words.Layout](../../../aspose.words.layout/)
* сборка [Aspose.Words](../../../)
