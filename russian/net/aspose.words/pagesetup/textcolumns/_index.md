---
title: PageSetup.TextColumns
linktitle: TextColumns
articleTitle: TextColumns
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PageSetup TextColumns, получите доступ к универсальной коллекции текстовых столбцов, чтобы без труда улучшить макет и форматирование документа.
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

* class [TextColumnCollection](../../textcolumncollection/)
* class [PageSetup](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
