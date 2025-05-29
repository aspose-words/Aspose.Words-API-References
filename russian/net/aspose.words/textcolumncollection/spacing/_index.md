---
title: TextColumnCollection.Spacing
linktitle: Spacing
articleTitle: Spacing
second_title: Aspose.Words для .NET
description: Откройте для себя свойство TextColumnCollection Spacing, легко управляйте интервалом между столбцами в пунктах для создания безупречного, профессионального макета. Улучшите свой дизайн сегодня!
type: docs
weight: 50
url: /ru/net/aspose.words/textcolumncollection/spacing/
---
## TextColumnCollection.Spacing property

Когда столбцы расположены равномерно, возвращает или задает величину пространства между каждым столбцом в пунктах.

```csharp
public double Spacing { get; set; }
```

## Примечания

Действует только тогда, когда[`EvenlySpaced`](../evenlyspaced/) установлен на`истинный` .

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
