---
title: ListCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words pour .NET
description: Accédez facilement aux éléments ListCollection par index. Simplifiez la gestion de vos données et optimisez votre codage grâce à cette puissante propriété !
type: docs
weight: 30
url: /fr/net/aspose.words.lists/listcollection/item/
---
## ListCollection indexer

Obtient une liste par index.

```csharp
public List this[int index] { get; }
```

## Exemples

Montre comment vérifier les propriétés du document propriétaire des listes.

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

Montre comment appliquer la mise en forme d'une liste existante à une collection de paragraphes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1");
builder.Writeln("Paragraph 2");
builder.Write("Paragraph 3");

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

Assert.AreEqual(0, paras.Count(n => ((Paragraph)n).ListFormat.IsListItem));

doc.Lists.Add(ListTemplate.NumberDefault);
List docList = doc.Lists[0];

foreach (Paragraph paragraph in paras.OfType<Paragraph>())
{
    paragraph.ListFormat.List = docList;
    paragraph.ListFormat.ListLevelNumber = 2;
}

Assert.AreEqual(3, paras.Count(n => ((Paragraph)n).ListFormat.IsListItem));
```

### Voir également

* class [List](../../list/)
* class [ListCollection](../)
* espace de noms [Aspose.Words.Lists](../../../aspose.words.lists/)
* Assemblée [Aspose.Words](../../../)
