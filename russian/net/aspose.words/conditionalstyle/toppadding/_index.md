---
title: ConditionalStyle.TopPadding
linktitle: TopPadding
articleTitle: TopPadding
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ConditionalStyle TopPadding, которое позволяет легко регулировать пространство над содержимым ячеек таблицы, улучшая компоновку и читабельность для лучшего дизайна.
type: docs
weight: 80
url: /ru/net/aspose.words/conditionalstyle/toppadding/
---
## ConditionalStyle.TopPadding property

Возвращает или задает размер пространства (в пунктах), добавляемого над содержимым ячеек таблицы.

```csharp
public double TopPadding { get; set; }
```

## Примеры

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

// Создать собственный стиль таблицы.
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");

// Условные стили — это изменения форматирования, которые затрагивают только некоторые ячейки таблицы.
// на основе предиката, например, нахождения ячеек в последней строке.
// Ниже приведены три способа доступа к условным стилям стиля таблицы из коллекции «ConditionalStyles».
// 1 - По типу стиля:
tableStyle.ConditionalStyles[ConditionalStyleType.FirstRow].Shading.BackgroundPatternColor = Color.AliceBlue;

// 2 - По индексу:
tableStyle.ConditionalStyles[0].Borders.Color = Color.Black;
tableStyle.ConditionalStyles[0].Borders.LineStyle = LineStyle.DotDash;
Assert.AreEqual(ConditionalStyleType.FirstRow, tableStyle.ConditionalStyles[0].Type);

// 3 - Как свойство:
tableStyle.ConditionalStyles.FirstRow.ParagraphFormat.Alignment = ParagraphAlignment.Center;

// Применить отступы и форматирование текста к условным стилям.
tableStyle.ConditionalStyles.LastRow.BottomPadding = 10;
tableStyle.ConditionalStyles.LastRow.LeftPadding = 10;
tableStyle.ConditionalStyles.LastRow.RightPadding = 10;
tableStyle.ConditionalStyles.LastRow.TopPadding = 10;
tableStyle.ConditionalStyles.LastColumn.Font.Bold = true;

// Перечислить все возможные условия стиля.
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

// Наш стиль применяет некоторые условные стили по умолчанию.
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands, 
    table.StyleOptions);

// Все остальные стили нам нужно будет включить самостоятельно через свойство «StyleOptions».
table.StyleOptions = table.StyleOptions | TableStyleOptions.LastRow | TableStyleOptions.LastColumn;

doc.Save(ArtifactsDir + "Table.ConditionalStyles.docx");
```

### Смотрите также

* class [ConditionalStyle](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
