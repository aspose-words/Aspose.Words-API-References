---
title: TextColumnCollection.Width
linktitle: Width
articleTitle: Width
second_title: Aspose.Words для .NET
description: Откройте для себя свойство TextColumnCollection Width. Легко управляйте равномерно распределенными столбцами для оптимальной компоновки и дизайна в ваших проектах.
type: docs
weight: 60
url: /ru/net/aspose.words/textcolumncollection/width/
---
## TextColumnCollection.Width property

Когда столбцы расположены равномерно, получает ширину столбцов.

```csharp
public double Width { get; }
```

## Примечания

Имеет эффект только тогда, когда[`EvenlySpaced`](../evenlyspaced/) установлен на`истинный`.

## Примеры

Показывает, как создать несколько равномерно распределенных столбцов в разделе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.Spacing = 100;
columns.SetCount(2);

builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");

doc.Save(ArtifactsDir + "PageSetup.ColumnsSameWidth.docx");
```

### Смотрите также

* class [TextColumnCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
