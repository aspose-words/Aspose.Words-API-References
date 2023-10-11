---
title: CompositeNode.GetText
second_title: Справочник по API Aspose.Words для .NET
description: CompositeNode метод. Получает текст этого узла и всех его дочерних элементов.
type: docs
weight: 130
url: /ru/net/aspose.words/compositenode/gettext/
---
## CompositeNode.GetText method

Получает текст этого узла и всех его дочерних элементов.

```csharp
public override string GetText()
```

### Примечания

Возвращенная строка включает все управляющие и специальные символы, как описано в разделе[`ControlChar`](../../controlchar/).

### Примеры

Показывает разницу между вызовом методов GetText и ToString на узле.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField("MERGEFIELD Field");

// GetText получит видимый текст, а также коды полей и специальные символы.
Assert.AreEqual("\u0013MERGEFIELD Field\u0014«Field»\u0015\u000c", doc.GetText());

// ToString вернет нам внешний вид документа, если он сохранен в переданном формате сохранения.
Assert.AreEqual("«Field»\r\n", doc.ToString(SaveFormat.Text));
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

foreach (Paragraph para in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem))
{ 
    Console.WriteLine($"This paragraph belongs to list ID# {para.ListFormat.List.ListId}, number style \"{para.ListFormat.ListLevel.NumberStyle}\"");
    Console.WriteLine($"\t\"{para.GetText().Trim()}\"");
}
```

### Смотрите также

* class [CompositeNode](../)
* пространство имен [Aspose.Words](../../compositenode/)
* сборка [Aspose.Words](../../../)


