---
title: ParagraphFormat.IsListItem
linktitle: IsListItem
articleTitle: IsListItem
second_title: Aspose.Words для .NET
description: Узнайте, как свойство ParagraphFormat IsListItem улучшает форматирование документа, легко определяя элементы маркированного или нумерованного списка.
type: docs
weight: 150
url: /ru/net/aspose.words/paragraphformat/islistitem/
---
## ParagraphFormat.IsListItem property

Истинно, когда абзац является элементом маркированного или нумерованного списка.

```csharp
public bool IsListItem { get; }
```

## Примеры

Показывает, как вложить список в другой список.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Список позволяет нам организовывать и украшать наборы абзацев с помощью префиксных символов и отступов.
 // Мы можем создавать вложенные списки, увеличивая уровень отступа.
 // Мы можем начать и закончить список, используя свойство "ListFormat" конструктора документов.
// Каждый абзац, который мы добавляем между началом и концом списка, станет элементом в списке.
// Создаем список-схему заголовков.
List outlineList = doc.Lists.Add(ListTemplate.OutlineNumbers);
builder.ListFormat.List = outlineList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("This is my Chapter 1");

// Создать нумерованный список.
List numberedList = doc.Lists.Add(ListTemplate.NumberDefault);
builder.ListFormat.List = numberedList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Writeln("Numbered list item 1.");

// Каждый абзац, составляющий список, будет иметь этот флаг.
Assert.True(builder.CurrentParagraph.IsListItem);
Assert.True(builder.ParagraphFormat.IsListItem);

// Создать маркированный список.
List bulletedList = doc.Lists.Add(ListTemplate.BulletDefault);
builder.ListFormat.List = bulletedList;
builder.ParagraphFormat.LeftIndent = 72;
builder.Writeln("Bulleted list item 1.");
builder.Writeln("Bulleted list item 2.");
builder.ParagraphFormat.ClearFormatting();

// Вернуться к нумерованному списку.
builder.ListFormat.List = numberedList;
builder.Writeln("Numbered list item 2.");
builder.Writeln("Numbered list item 3.");

// Вернуться к списку структур.
builder.ListFormat.List = outlineList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("This is my Chapter 2");

builder.ParagraphFormat.ClearFormatting();

builder.Document.Save(ArtifactsDir + "Lists.NestedLists.docx");
```

### Смотрите также

* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
