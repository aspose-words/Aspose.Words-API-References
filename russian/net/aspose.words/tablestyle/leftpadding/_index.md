---
title: TableStyle.LeftPadding
linktitle: LeftPadding
articleTitle: LeftPadding
second_title: Aspose.Words для .NET
description: Откройте для себя свойство TableStyle LeftPadding, чтобы настроить макет ячейки таблицы. Легко настройте левый интервал для изысканного, профессионального вида.
type: docs
weight: 100
url: /ru/net/aspose.words/tablestyle/leftpadding/
---
## TableStyle.LeftPadding property

Возвращает или задает размер пространства (в пунктах), добавляемого слева от содержимого ячеек таблицы.

```csharp
public double LeftPadding { get; set; }
```

## Примеры

Показывает, как создать пользовательские настройки стиля для таблицы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Name");
builder.InsertCell();
builder.Write("مرحبًا");
builder.EndRow();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.AllowBreakAcrossPages = true;
tableStyle.Bidi = true;
tableStyle.CellSpacing = 5;
tableStyle.BottomPadding = 20;
tableStyle.LeftPadding = 5;
tableStyle.RightPadding = 10;
tableStyle.TopPadding = 20;
tableStyle.Shading.BackgroundPatternColor = Color.AntiqueWhite;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.DotDash;
tableStyle.VerticalAlignment = CellVerticalAlignment.Center;

table.Style = tableStyle;

// Установка свойств стиля таблицы может повлиять на свойства самой таблицы.
Assert.True(table.Bidi);
Assert.AreEqual(5.0d, table.CellSpacing);
Assert.AreEqual("MyTableStyle1", table.StyleName);

doc.Save(ArtifactsDir + "Table.TableStyleCreation.docx");
```

### Смотрите также

* class [TableStyle](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
