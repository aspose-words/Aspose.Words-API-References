---
title: List.ListId
linktitle: ListId
articleTitle: ListId
second_title: Aspose.Words för .NET
description: Upptäck den unika ListId-egenskapen för att enkelt komma åt och hantera dina listor. Effektivisera ditt arbetsflöde med denna viktiga identifierare.
type: docs
weight: 60
url: /sv/net/aspose.words.lists/list/listid/
---
## List.ListId property

Hämtar listans unika identifierare.

```csharp
public int ListId { get; }
```

## Anmärkningar

Normalt sett behöver du inte använda den här egenskapen. Men om du använder den gör du det normalt tillsammans med[`GetListByListId`](../../listcollection/getlistbylistid/) metod för att hitta en -lista med hjälp av dess identifierare.

## Exempel

Visar hur man verifierar egenskaper för ägardokument för listor.

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

Visar hur man skriver ut alla stycken i ett dokument som är listobjekt.

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

### Se även

* class [List](../)
* namnutrymme [Aspose.Words.Lists](../../../aspose.words.lists/)
* hopsättning [Aspose.Words](../../../)
