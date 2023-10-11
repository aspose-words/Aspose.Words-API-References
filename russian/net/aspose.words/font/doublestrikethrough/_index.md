---
title: Font.DoubleStrikeThrough
second_title: Справочник по API Aspose.Words для .NET
description: Font свойство. True если шрифт отформатирован как текст с двойным зачеркиванием.
type: docs
weight: 90
url: /ru/net/aspose.words/font/doublestrikethrough/
---
## Font.DoubleStrikeThrough property

True, если шрифт отформатирован как текст с двойным зачеркиванием.

```csharp
public bool DoubleStrikeThrough { get; set; }
```

### Примеры

Показывает, как добавить зачеркивание строки в текст.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

Run run = new Run(doc, "Text with a single-line strikethrough.");
run.Font.StrikeThrough = true;
para.AppendChild(run);

para = (Paragraph)para.ParentNode.AppendChild(new Paragraph(doc));

run = new Run(doc, "Text with a double-line strikethrough.");
run.Font.DoubleStrikeThrough = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.StrikeThrough.docx");
```

### Смотрите также

* class [Font](../)
* пространство имен [Aspose.Words](../../font/)
* сборка [Aspose.Words](../../../)


