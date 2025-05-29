---
title: Font.StrikeThrough
linktitle: StrikeThrough
articleTitle: StrikeThrough
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Font StrikeThrough. Легко форматируйте текст с помощью зачеркивания для четкого визуального акцента в ваших проектах. Улучшите читаемость сегодня!
type: docs
weight: 400
url: /ru/net/aspose.words/font/strikethrough/
---
## Font.StrikeThrough property

True, если шрифт отформатирован как зачеркнутый текст.

```csharp
public bool StrikeThrough { get; set; }
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
