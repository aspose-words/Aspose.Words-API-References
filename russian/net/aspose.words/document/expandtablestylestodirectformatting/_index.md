---
title: Document.ExpandTableStylesToDirectFormatting
linktitle: ExpandTableStylesToDirectFormatting
articleTitle: ExpandTableStylesToDirectFormatting
second_title: Aspose.Words для .NET
description: Преобразуйте стили таблиц в прямое форматирование с помощью метода ExpandTableStylesToDirectFormatting, улучшив внешний вид вашего документа без особых усилий.
type: docs
weight: 630
url: /ru/net/aspose.words/document/expandtablestylestodirectformatting/
---
## Document.ExpandTableStylesToDirectFormatting method

Преобразует форматирование, указанное в стилях таблиц, в прямое форматирование таблиц в документе.

```csharp
public void ExpandTableStylesToDirectFormatting()
```

## Примечания

Этот метод существует, поскольку эта версия Aspose.Words обеспечивает только ограниченную поддержку стилей таблиц (см. ниже). Этот метод может быть полезен при загрузке документа DOCX или WordprocessingML , содержащего таблицы, отформатированные с помощью стилей таблиц, и вам необходимо запросить форматирование таблиц , ячеек, абзацев или текста.

Эта версия Aspose.Words обеспечивает ограниченную поддержку следующих стилей таблиц:

* Стили таблиц, определенные в документах DOCX или WordprocessingML, сохраняются как table styles при сохранении документа как DOCX или WordprocessingML.
* Стили таблиц, определенные в документах DOCX или WordprocessingML, автоматически преобразуются в прямое форматирование таблиц при сохранении документа в любом другом формате, визуализации или печати.
* Стили таблиц, определенные в документах DOC, сохраняются как стили таблиц только при сохранении документа как DOC.

## Примеры

Показывает, как применить свойства стиля таблицы непосредственно к элементам таблицы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Hello world!");
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.RowStripe = 3;
tableStyle.CellSpacing = 5;
tableStyle.Shading.BackgroundPatternColor = Color.AntiqueWhite;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.DotDash;

table.Style = tableStyle;

// Этот метод касается свойств стиля таблицы, таких как те, которые мы установили выше.
doc.ExpandTableStylesToDirectFormatting();

doc.Save(ArtifactsDir + "Document.TableStyleToDirectFormatting.docx");
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
