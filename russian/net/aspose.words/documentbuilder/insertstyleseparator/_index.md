---
title: DocumentBuilder.InsertStyleSeparator
second_title: Справочник по API Aspose.Words для .NET
description: DocumentBuilder метод. Вставляет в документ разделитель стилей.
type: docs
weight: 460
url: /ru/net/aspose.words/documentbuilder/insertstyleseparator/
---
## DocumentBuilder.InsertStyleSeparator method

Вставляет в документ разделитель стилей.

```csharp
public void InsertStyleSeparator()
```

### Примечания

Этот метод позволяет применять разные стили абзаца к двум разным частям текстовой строки.

### Примеры

Показывает, как работать с разделителями стилей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Каждый абзац может иметь только один стиль.
// Метод InsertStyleSeparator позволяет обойти это ограничение.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Write("This text is in a Heading style. ");
builder.InsertStyleSeparator();

Style paraStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyParaStyle");
paraStyle.Font.Bold = false;
paraStyle.Font.Size = 8;
paraStyle.Font.Name = "Arial";

builder.ParagraphFormat.StyleName = paraStyle.Name;
builder.Write("This text is in a custom style. ");

// Вызов метода InsertStyleSeparator создает еще один абзац,
// который может иметь стиль, отличный от предыдущего. Разрыва между абзацами не будет.
// Текст в выходном документе будет выглядеть как один абзац с двумя стилями.
Assert.AreEqual(2, doc.FirstSection.Body.Paragraphs.Count);
Assert.AreEqual("Heading 1", doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.Style.Name);
Assert.AreEqual("MyParaStyle", doc.FirstSection.Body.Paragraphs[1].ParagraphFormat.Style.Name);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertStyleSeparator.docx");
```

### Смотрите также

* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../documentbuilder/)
* сборка [Aspose.Words](../../../)


