---
title: TextColumnCollection.SetCount
linktitle: SetCount
articleTitle: SetCount
second_title: Aspose.Words для .NET
description: TextColumnCollection SetCount метод. Упорядочивает текст в указанное количество текстовых столбцов на С#.
type: docs
weight: 70
url: /ru/net/aspose.words/textcolumncollection/setcount/
---
## TextColumnCollection.SetCount method

Упорядочивает текст в указанное количество текстовых столбцов.

```csharp
public void SetCount(int newCount)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| newCount | Int32 | Количество столбцов, в которых будет размещен текст. |

## Примечания

Когда[`EvenlySpaced`](../evenlyspaced/) является`ЛОЖЬ` и вы увеличиваете количество столбцов, new[`TextColumn`](../../textcolumn/) объекты создаются с нулевой шириной и интервалом. Вам необходимо установить ширину и интервал для новых столбцов.

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

* class [TextColumnCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
