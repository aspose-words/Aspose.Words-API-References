---
title: TextColumnCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words для .NET
description: Откройте для себя свойство TextColumnCollection Count, чтобы легко получить доступ к количеству столбцов в разделе документа для улучшенного управления макетом.
type: docs
weight: 10
url: /ru/net/aspose.words/textcolumncollection/count/
---
## TextColumnCollection.Count property

Получает количество столбцов в разделе документа.

```csharp
public int Count { get; }
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

* class [TextColumnCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
