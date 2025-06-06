---
title: TableStyle.Shading
linktitle: Shading
articleTitle: Shading
second_title: Aspose.Words для .NET
description: Откройте для себя свойство TableStyle Shading, чтобы улучшить ячейки таблицы с помощью настраиваемого форматирования заливки для придания ей изысканного, профессионального вида.
type: docs
weight: 130
url: /ru/net/aspose.words/tablestyle/shading/
---
## TableStyle.Shading property

Получает[`Shading`](../../shading/) объект, который ссылается на форматирование затенения ячеек таблицы.

```csharp
public Shading Shading { get; }
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

* class [Shading](../../shading/)
* class [TableStyle](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
