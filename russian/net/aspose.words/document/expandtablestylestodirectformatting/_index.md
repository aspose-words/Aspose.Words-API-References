---
title: ExpandTableStylesToDirectFormatting
second_title: Справочник по API Aspose.Words для .NET
description: Преобразует форматирование указанное в стилях таблиц в прямое форматирование таблиц в документе.
type: docs
weight: 570
url: /ru/net/aspose.words/document/expandtablestylestodirectformatting/
---
## Document.ExpandTableStylesToDirectFormatting method

Преобразует форматирование, указанное в стилях таблиц, в прямое форматирование таблиц в документе.

```csharp
public void ExpandTableStylesToDirectFormatting()
```

### Примечания

Этот метод существует, потому что эта версия Aspose.Words предоставляет только ограниченную поддержку стилей таблиц (см. ниже). Этот метод может быть полезен, когда вы загружаете документ DOCX или WordprocessingML , который содержит таблицы, отформатированные с помощью стилей таблиц, и вам нужно запросить форматирование таблиц, ячеек, абзацев или текста .

Эта версия Aspose.Words обеспечивает ограниченную поддержку следующих стилей таблиц:

* Стили таблиц, определенные в документах DOCX или WordprocessingML, сохраняются как таблицы styles при сохранении документа в формате DOCX или WordprocessingML.
* Стили таблиц, определенные в документах DOCX или WordprocessingML, автоматически преобразовываются в прямое форматирование таблиц при сохранении документа в любом другом формате, рендеринге или печати.
* Стили таблиц, определенные в документах DOC, сохраняются как стили таблиц при сохранении документа только как DOC.

### Примеры

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

// Этот метод относится к свойствам стиля таблицы, таким как те, которые мы установили выше.
doc.ExpandTableStylesToDirectFormatting();

doc.Save(ArtifactsDir + "Document.TableStyleToDirectFormatting.docx");
```

### Смотрите также

* class [Document](../../document)
* пространство имен [Aspose.Words](../../document)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->