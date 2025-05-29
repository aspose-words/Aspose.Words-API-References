---
title: TableStyle.Alignment
linktitle: Alignment
articleTitle: Alignment
second_title: Aspose.Words для .NET
description: Откройте для себя свойство выравнивания TableStyle, чтобы легко настроить макет таблицы и улучшить ее визуальную привлекательность, придав ей профессиональный вид.
type: docs
weight: 10
url: /ru/net/aspose.words/tablestyle/alignment/
---
## TableStyle.Alignment property

Задает выравнивание для стиля таблицы.

```csharp
public TableAlignment Alignment { get; set; }
```

## Примечания

Значение по умолчанию:Left .

## Примеры

Показывает, как задать положение таблицы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены два способа выравнивания таблицы по горизонтали.
// 1 - Используйте свойство "Alignment", чтобы выровнять его по месту на странице, например по центру:
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.Alignment = TableAlignment.Center;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.Single;

// Вставляем таблицу и применяем к ней созданный нами стиль.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Aligned to the center of the page");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

table.Style = tableStyle;

// 2 - Используйте «LeftIndent», чтобы указать отступ от левого поля страницы:
tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle2");
tableStyle.LeftIndent = 55;
tableStyle.Borders.Color = Color.Green;
tableStyle.Borders.LineStyle = LineStyle.Single;

table = builder.StartTable();
builder.InsertCell();
builder.Write("Aligned according to left indent");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

table.Style = tableStyle;

doc.Save(ArtifactsDir + "Table.SetTableAlignment.docx");
```

### Смотрите также

* enum [TableAlignment](../../../aspose.words.tables/tablealignment/)
* class [TableStyle](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
