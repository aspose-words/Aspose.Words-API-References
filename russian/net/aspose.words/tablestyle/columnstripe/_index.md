---
title: TableStyle.ColumnStripe
linktitle: ColumnStripe
articleTitle: ColumnStripe
second_title: Aspose.Words для .NET
description: Откройте для себя свойство TableStyle ColumnStripe, которое позволяет легко настраивать чередование четных и нечетных столбцов, придавая таблицам изысканный и профессиональный вид.
type: docs
weight: 70
url: /ru/net/aspose.words/tablestyle/columnstripe/
---
## TableStyle.ColumnStripe property

Возвращает или задает количество столбцов, включаемых в полосу, когда стиль задает полосу четных/нечетных столбцов.

```csharp
public int ColumnStripe { get; set; }
```

## Примеры

Показывает, как создавать условные стили таблиц, чередующиеся между строками.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Мы можем настроить условный стиль таблицы, чтобы применить другой цвет к строке/столбцу,
// в зависимости от того, является ли строка/столбец четным или нечетным, создавая чередующийся цветовой узор.
// Мы также можем применить число n к полосе строк/столбцов,
// это означает, что цвет меняется через каждые n строк/столбцов, а не через один.
// Создадим таблицу, в которой отдельные столбцы и строки будут объединены в группы, а столбцы — в группы по три.
Table table = builder.StartTable();
for (int i = 0; i < 15; i++)
{
    for (int j = 0; j < 4; j++)
    {
        builder.InsertCell();
        builder.Writeln($"{(j % 2 == 0 ? "Even" : "Odd")} column.");
        builder.Write($"Row banding {(i % 3 == 0 ? "start" : "continuation")}.");
    }
    builder.EndRow();
}
builder.EndTable();

// Применяем стиль линии ко всем границам таблицы.
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.Borders.Color = Color.Black;
tableStyle.Borders.LineStyle = LineStyle.Double;

// Устанавливаем два цвета, которые будут чередоваться через каждые три ряда.
tableStyle.RowStripe = 3;
tableStyle.ConditionalStyles[ConditionalStyleType.OddRowBanding].Shading.BackgroundPatternColor = Color.LightBlue;
tableStyle.ConditionalStyles[ConditionalStyleType.EvenRowBanding].Shading.BackgroundPatternColor = Color.LightCyan;

// Задайте цвет для каждого четного столбца, который переопределит любую пользовательскую раскраску строк.
tableStyle.ColumnStripe = 1;
tableStyle.ConditionalStyles[ConditionalStyleType.EvenColumnBanding].Shading.BackgroundPatternColor = Color.LightSalmon;

table.Style = tableStyle;

// Свойство "StyleOptions" по умолчанию включает полосу строк.
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands,
    table.StyleOptions);

// Используйте свойство "StyleOptions" также для включения полосирования столбцов.
table.StyleOptions = table.StyleOptions | TableStyleOptions.ColumnBands;

doc.Save(ArtifactsDir + "Table.AlternatingRowStyles.docx");
```

### Смотрите также

* class [TableStyle](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
