---
title: List.ListId
second_title: Справочник по API Aspose.Words для .NET
description: List свойство. Получает уникальный идентификатор списка.
type: docs
weight: 60
url: /ru/net/aspose.words.lists/list/listid/
---
## List.ListId property

Получает уникальный идентификатор списка.

```csharp
public int ListId { get; }
```

### Примечания

Обычно вам не нужно использовать это свойство. Но если вы используете его, вы обычно делаете так в сочетании с[`GetListByListId`](../../listcollection/getlistbylistid/) метод поиска списка a по его идентификатору.

### Примеры

Показывает, как проверить свойства документа владельца списков.

```csharp
Document doc = new Document();

ListCollection lists = doc.Lists;

Assert.AreEqual(doc, lists.Document);

List list = lists.Add(ListTemplate.BulletDefault);

Assert.AreEqual(doc, list.Document);

Console.WriteLine("Current list count: " + lists.Count);
Console.WriteLine("Is the first document list: " + (lists[0].Equals(list)));
Console.WriteLine("ListId: " + list.ListId);
Console.WriteLine("List is the same by ListId: " + (lists.GetListByListId(1).Equals(list)));
```

Показывает, как вывести все абзацы в документе, которые являются элементами списка.

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

* class [List](../)
* пространство имен [Aspose.Words.Lists](../../list/)
* сборка [Aspose.Words](../../../)


