---
title: TextColumnCollection.SetCount
linktitle: SetCount
articleTitle: SetCount
second_title: Aspose.Words для .NET
description: Оптимизируйте макет с помощью метода TextColumnCollection SetCount, который легко размещает текст в нужном количестве столбцов для повышения удобства чтения.
type: docs
weight: 70
url: /ru/net/aspose.words/textcolumncollection/setcount/
---
## TextColumnCollection.SetCount method

Располагает текст в указанном количестве текстовых столбцов.

```csharp
public void SetCount(int newCount)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| newCount | Int32 | Количество столбцов, в которые должен быть разбит текст. |

## Примечания

Когда[`EvenlySpaced`](../evenlyspaced/) является`ЛОЖЬ` и вы увеличиваете количество столбцов, new[`TextColumn`](../../textcolumn/) объекты создаются с нулевой шириной и интервалом. Вам необходимо задать ширину и интервал для новых столбцов.

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
