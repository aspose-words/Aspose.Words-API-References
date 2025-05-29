---
title: List.ListId
linktitle: ListId
articleTitle: ListId
second_title: Aspose.Words für .NET
description: Entdecken Sie die einzigartige ListId-Eigenschaft für einfachen Zugriff und Verwaltung Ihrer Listen. Optimieren Sie Ihren Workflow mit dieser wichtigen Kennung.
type: docs
weight: 60
url: /de/net/aspose.words.lists/list/listid/
---
## List.ListId property

Ruft die eindeutige Kennung der Liste ab.

```csharp
public int ListId { get; }
```

## Bemerkungen

Normalerweise müssen Sie diese Eigenschaft nicht verwenden. Wenn Sie sie jedoch verwenden, tun Sie dies normalerweise in Verbindung mit dem[`GetListByListId`](../../listcollection/getlistbylistid/) Methode zum Suchen einer -Liste anhand ihrer Kennung.

## Beispiele

Zeigt, wie die Eigentümerdokumenteigenschaften von Listen überprüft werden.

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

Zeigt, wie alle Absätze in einem Dokument ausgegeben werden, die Listenelemente sind.

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

### Siehe auch

* class [List](../)
* namensraum [Aspose.Words.Lists](../../../aspose.words.lists/)
* Montage [Aspose.Words](../../../)
