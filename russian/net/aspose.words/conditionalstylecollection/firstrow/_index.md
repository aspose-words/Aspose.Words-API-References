---
title: ConditionalStyleCollection.FirstRow
second_title: Справочник по API Aspose.Words для .NET
description: ConditionalStyleCollection свойство. Получает стиль первой строки.
type: docs
weight: 70
url: /ru/net/aspose.words/conditionalstylecollection/firstrow/
---
## ConditionalStyleCollection.FirstRow property

Получает стиль первой строки.

```csharp
public ConditionalStyle FirstRow { get; }
```

### Примеры

Показывает, как работать с определенными стилями областей таблицы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndRow();
builder.InsertCell();
builder.Write("Cell 3");
builder.InsertCell();
builder.Write("Cell 4");
builder.EndTable();

// Создаем пользовательский стиль таблицы.
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");

// Условные стили — это изменения форматирования, которые влияют только на некоторые ячейки таблицы
// на основе предиката, такого как ячейки, находящиеся в последней строке.
// Ниже приведены три способа доступа к условным стилям табличного стиля из коллекции «ConditionalStyles».
// 1 - По типу стиля:
tableStyle.ConditionalStyles[ConditionalStyleType.FirstRow].Shading.BackgroundPatternColor = Color.AliceBlue;

// 2 - По индексу:
tableStyle.ConditionalStyles[0].Borders.Color = Color.Black;
tableStyle.ConditionalStyles[0].Borders.LineStyle = LineStyle.DotDash;
Assert.AreEqual(ConditionalStyleType.FirstRow, tableStyle.ConditionalStyles[0].Type);

// 3 - Как свойство:
tableStyle.ConditionalStyles.FirstRow.ParagraphFormat.Alignment = ParagraphAlignment.Center;

// Применение отступов и форматирования текста к условным стилям.
tableStyle.ConditionalStyles.LastRow.BottomPadding = 10;
tableStyle.ConditionalStyles.LastRow.LeftPadding = 10;
tableStyle.ConditionalStyles.LastRow.RightPadding = 10;
tableStyle.ConditionalStyles.LastRow.TopPadding = 10;
tableStyle.ConditionalStyles.LastColumn.Font.Bold = true;

// Список всех возможных условий стиля.
using (IEnumerator<ConditionalStyle> enumerator = tableStyle.ConditionalStyles.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        ConditionalStyle currentStyle = enumerator.Current;
        if (currentStyle != null) Console.WriteLine(currentStyle.Type);
    }
}

// Применяем к таблице пользовательский стиль, содержащий все условные стили.
table.Style = tableStyle;

// Наш стиль по умолчанию применяет некоторые условные стили.
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands, 
    table.StyleOptions);

// Нам нужно будет включить все остальные стили самостоятельно через свойство StyleOptions.
table.StyleOptions = table.StyleOptions | TableStyleOptions.LastRow | TableStyleOptions.LastColumn;

doc.Save(ArtifactsDir + "Table.ConditionalStyles.docx");
```

### Смотрите также

* class [ConditionalStyle](../../conditionalstyle/)
* class [ConditionalStyleCollection](../)
* пространство имен [Aspose.Words](../../conditionalstylecollection/)
* сборка [Aspose.Words](../../../)


