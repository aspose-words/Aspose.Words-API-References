---
title: Paragraph.BreakIsStyleSeparator
linktitle: BreakIsStyleSeparator
articleTitle: BreakIsStyleSeparator
second_title: Aspose.Words для .NET
description: Узнайте, как свойство Paragraph Break IsStyleSeparator улучшает форматирование документа, позволяя использовать смешанные стили абзацев для большей гибкости дизайна.
type: docs
weight: 20
url: /ru/net/aspose.words/paragraph/breakisstyleseparator/
---
## Paragraph.BreakIsStyleSeparator property

True, если этот разрыв абзаца является разделителем стилей. Разделитель стилей позволяет одному абзацу состоять из частей, имеющих разные стили абзацев.

```csharp
public bool BreakIsStyleSeparator { get; }
```

## Примеры

Показывает, как написать текст в той же строке, что и заголовок оглавления, и чтобы он не отображался в оглавлении.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertTableOfContents("\\o \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Вставьте абзац со стилем, который оглавление воспримет как запись.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

// Обе эти строки находятся в одном абзаце и поэтому будут отображаться в одной и той же записи оглавления.
builder.Write("Heading 1. ");
builder.Write("Will appear in the TOC. ");

// Если мы вставим разделитель стилей, мы сможем написать больше текста в том же абзаце
// и использовать другой стиль, не отображая его в оглавлении.
// Если мы используем стиль заголовка после разделителя, мы можем нарисовать несколько записей оглавления из одной текстовой строки документа.
builder.InsertStyleSeparator();
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Quote;
builder.Write("Won't appear in the TOC. ");

Assert.True(doc.FirstSection.Body.FirstParagraph.BreakIsStyleSeparator);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Paragraph.BreakIsStyleSeparator.docx");
```

### Смотрите также

* class [Paragraph](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
