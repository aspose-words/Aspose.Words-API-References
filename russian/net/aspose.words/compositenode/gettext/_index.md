---
title: CompositeNode.GetText
linktitle: GetText
articleTitle: GetText
second_title: Aspose.Words для .NET
description: Откройте для себя метод CompositeNode GetText для эффективного извлечения текста из узлов и их дочерних элементов, расширяя ваши возможности обработки данных.
type: docs
weight: 130
url: /ru/net/aspose.words/compositenode/gettext/
---
## CompositeNode.GetText method

Получает текст этого узла и всех его дочерних узлов.

```csharp
public override string GetText()
```

## Примечания

Возвращаемая строка включает все управляющие и специальные символы, как описано в[`ControlChar`](../../controlchar/).

## Примеры

Показывает разницу между вызовом методов GetText и ToString на узле.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField("MERGEFIELD Field");

// GetText извлечет видимый текст, а также коды полей и специальные символы.
Assert.AreEqual("\u0013MERGEFIELD Field\u0014«Field»\u0015", doc.GetText().Trim());

// ToString вернет нам внешний вид документа, сохраненного в переданном формате сохранения.
Assert.AreEqual("«Field»", doc.ToString(SaveFormat.Text).Trim());
```

Показывает, как вывести все абзацы документа, являющиеся элементами списка.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.ApplyNumberDefault();
builder.Writeln("Numbered list item 1");
builder.Writeln("Numbered list item 2");
builder.Writeln("Numbered list item 3");
builder.ListFormat.RemoveNumbers();

builder.ListFormat.ApplyBulletDefault();
builder.Writeln("Bulleted list item 1");
builder.Writeln("Bulleted list item 2");
builder.Writeln("Bulleted list item 3");
builder.ListFormat.RemoveNumbers();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

foreach (Paragraph para in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem).ToList())
{ 
    Console.WriteLine($"This paragraph belongs to list ID# {para.ListFormat.List.ListId}, number style \"{para.ListFormat.ListLevel.NumberStyle}\"");
    Console.WriteLine($"\t\"{para.GetText().Trim()}\"");
}
```

### Смотрите также

* class [CompositeNode](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
