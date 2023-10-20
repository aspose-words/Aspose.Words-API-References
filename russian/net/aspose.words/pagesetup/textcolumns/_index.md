---
title: PageSetup.TextColumns
linktitle: TextColumns
articleTitle: TextColumns
second_title: Aspose.Words для .NET
description: PageSetup TextColumns свойство. Возвращает коллекцию представляющую набор текстовых столбцов на С#.
type: docs
weight: 420
url: /ru/net/aspose.words/pagesetup/textcolumns/
---
## PageSetup.TextColumns property

Возвращает коллекцию, представляющую набор текстовых столбцов.

```csharp
public TextColumnCollection TextColumns { get; }
```

## Примеры

Показывает, как создать в разделе несколько равномерно расположенных столбцов.

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

* class [TextColumnCollection](../../textcolumncollection/)
* class [PageSetup](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
