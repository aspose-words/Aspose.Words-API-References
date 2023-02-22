---
title: TextColumnCollection.Spacing
second_title: Справочник по API Aspose.Words для .NET
description: TextColumnCollection свойство. Когда столбцы расположены равномерно получает или задает расстояние между каждым столбцом в пунктах.
type: docs
weight: 50
url: /ru/net/aspose.words/textcolumncollection/spacing/
---
## TextColumnCollection.Spacing property

Когда столбцы расположены равномерно, получает или задает расстояние между каждым столбцом в пунктах.

```csharp
public double Spacing { get; set; }
```

### Примечания

Действует только когда[`EvenlySpaced`](../evenlyspaced/) установлен на **истинный** .

### Примеры

Показывает, как создать несколько равномерно расположенных столбцов в разделе.

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
* пространство имен [Aspose.Words](../../textcolumncollection/)
* сборка [Aspose.Words](../../../)


