---
title: List.ListId
linktitle: ListId
articleTitle: ListId
second_title: Aspose.Words pour .NET
description: Découvrez la propriété unique ListId pour accéder et gérer facilement vos listes. Simplifiez votre flux de travail grâce à cet identifiant essentiel.
type: docs
weight: 60
url: /fr/net/aspose.words.lists/list/listid/
---
## List.ListId property

Obtient l'identifiant unique de la liste.

```csharp
public int ListId { get; }
```

## Remarques

Vous n'avez généralement pas besoin d'utiliser cette propriété. Cependant, si vous l'utilisez, vous le faites généralement en conjonction avec la propriété so .[`GetListByListId`](../../listcollection/getlistbylistid/) méthode pour trouver une liste a par son identifiant.

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

Montre comment générer tous les paragraphes d'un document qui sont des éléments de liste.

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

### Voir également

* class [List](../)
* espace de noms [Aspose.Words.Lists](../../../aspose.words.lists/)
* Assemblée [Aspose.Words](../../../)
