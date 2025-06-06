---
title: Font.DoubleStrikeThrough
linktitle: DoubleStrikeThrough
articleTitle: DoubleStrikeThrough
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Font DoubleStrikeThrough. Легко форматируйте текст с помощью двойного зачеркивания для большей ясности и стиля в ваших документах.
type: docs
weight: 90
url: /ru/net/aspose.words/font/doublestrikethrough/
---
## Font.DoubleStrikeThrough property

True, если шрифт отформатирован как двойной зачеркнутый текст.

```csharp
public bool DoubleStrikeThrough { get; set; }
```

## Примеры

Показывает, как добавить зачеркнутую линию к тексту.

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
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
