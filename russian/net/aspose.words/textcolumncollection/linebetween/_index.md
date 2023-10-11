---
title: TextColumnCollection.LineBetween
second_title: Справочник по API Aspose.Words для .NET
description: TextColumnCollection свойство. Когдаистинный добавляет вертикальную линию между столбцами.
type: docs
weight: 40
url: /ru/net/aspose.words/textcolumncollection/linebetween/
---
## TextColumnCollection.LineBetween property

Когда`истинный` добавляет вертикальную линию между столбцами.

```csharp
public bool LineBetween { get; set; }
```

### Примеры

Показывает, как разделить столбцы вертикальной линией.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Настройте объект PageSetup текущего раздела, чтобы разделить текст на несколько столбцов.
// Установите для свойства LineBetween значение true, чтобы разместить разделительную линию между столбцами.
// Установите для свойства LineBetween значение false, чтобы оставить пространство между столбцами пустым.
TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.LineBetween = lineBetween;
columns.SetCount(3);

builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 3.");

doc.Save(ArtifactsDir + "PageSetup.VerticalLineBetweenColumns.docx");
```

### Смотрите также

* class [TextColumnCollection](../)
* пространство имен [Aspose.Words](../../textcolumncollection/)
* сборка [Aspose.Words](../../../)


