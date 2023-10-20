---
title: TableStyle.ColumnStripe
linktitle: ColumnStripe
articleTitle: ColumnStripe
second_title: Aspose.Words для .NET
description: TableStyle ColumnStripe свойство. Получает или задает количество столбцов которые необходимо включить в группировку когда стиль определяет группировку нечетных/четных столбцов на С#.
type: docs
weight: 70
url: /ru/net/aspose.words/tablestyle/columnstripe/
---
## TableStyle.ColumnStripe property

Получает или задает количество столбцов, которые необходимо включить в группировку, когда стиль определяет группировку нечетных/четных столбцов.

```csharp
public int ColumnStripe { get; set; }
```

## Примеры

Показывает, как создавать стили условных таблиц, которые чередуются между строками.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Мы можем настроить условный стиль таблицы, чтобы применить другой цвет к строке/столбцу,
// в зависимости от того, является ли строка/столбец четной или нечетной, создается шаблон чередующегося цвета.
// Мы также можем применить число n к полосе строк/столбцов,
// это означает, что цвет меняется после каждых n строк/столбцов вместо одной.
// Создайте таблицу, в которой отдельные столбцы и строки будут объединены в группы, а столбцы будут объединены в тройки.
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

// Устанавливаем два цвета, которые будут чередоваться через каждые 3 строки.
tableStyle.RowStripe = 3;
tableStyle.ConditionalStyles[ConditionalStyleType.OddRowBanding].Shading.BackgroundPatternColor = Color.LightBlue;
tableStyle.ConditionalStyles[ConditionalStyleType.EvenRowBanding].Shading.BackgroundPatternColor = Color.LightCyan;

// Установите цвет, который будет применяться к каждому четному столбцу, который будет переопределять любую пользовательскую окраску строк.
tableStyle.ColumnStripe = 1;
tableStyle.ConditionalStyles[ConditionalStyleType.EvenColumnBanding].Shading.BackgroundPatternColor = Color.LightSalmon;

table.Style = tableStyle;

// Свойство «StyleOptions» по умолчанию включает объединение строк.
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands,
    table.StyleOptions);

// Используйте также свойство StyleOptions, чтобы включить объединение столбцов.
table.StyleOptions = table.StyleOptions | TableStyleOptions.ColumnBands;

doc.Save(ArtifactsDir + "Table.AlternatingRowStyles.docx");
```

### Смотрите также

* class [TableStyle](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
