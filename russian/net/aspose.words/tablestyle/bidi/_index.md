---
title: TableStyle.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: Aspose.Words для .NET
description: Откройте для себя свойство TableStyle Bidi, которое позволяет легко управлять стилями таблиц с направлением письма справа налево, улучшая макет для лучшей читабельности и удобства для пользователей.
type: docs
weight: 30
url: /ru/net/aspose.words/tablestyle/bidi/
---
## TableStyle.Bidi property

Возвращает или задает, является ли это стилем для таблицы с направлением справа налево.

```csharp
public bool Bidi { get; set; }
```

## Примечания

Когда`истинный`, ячейки в рядах располагаются справа налево.

Значение по умолчанию:`ЛОЖЬ`.

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
