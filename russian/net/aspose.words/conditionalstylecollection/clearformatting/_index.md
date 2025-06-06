---
title: ConditionalStyleCollection.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words для .NET
description: Узнайте, как метод ConditionalStyleCollection ClearFormatting эффективно удаляет все условные стили из вашей таблицы, повышая ясность и улучшая дизайн.
type: docs
weight: 150
url: /ru/net/aspose.words/conditionalstylecollection/clearformatting/
---
## ConditionalStyleCollection.ClearFormatting method

Очищает все условные стили таблицы style.

```csharp
public void ClearFormatting()
```

## Примеры

Показывает, как сбросить условные стили таблиц.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("First row");
builder.EndRow();
builder.InsertCell();
builder.Write("Last row");
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
table.Style = tableStyle;

// Задаем стиль таблицы, чтобы окрасить границы первой строки таблицы в красный цвет.
tableStyle.ConditionalStyles.FirstRow.Borders.Color = Color.Red;

// Задаем стиль таблицы, чтобы окрасить границы последней строки таблицы в синий цвет.
tableStyle.ConditionalStyles.LastRow.Borders.Color = Color.Blue;

// Ниже приведены два способа использования метода «ClearFormatting» для очистки условных стилей.
// 1 — Очистить условные стили для определенной части таблицы:
tableStyle.ConditionalStyles[0].ClearFormatting();

Assert.AreEqual(Color.Empty, tableStyle.ConditionalStyles.FirstRow.Borders.Color);

// 2 - Очистить условные стили для всей таблицы:
tableStyle.ConditionalStyles.ClearFormatting();

Assert.True(tableStyle.ConditionalStyles.All(s => s.Borders.Color == Color.Empty));
```

### Смотрите также

* class [ConditionalStyleCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
