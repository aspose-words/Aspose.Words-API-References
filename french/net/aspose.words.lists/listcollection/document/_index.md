---
title: ListCollection.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Document ListCollection pour accéder facilement au document propriétaire et optimiser la gestion de vos données. Gagnez en efficacité dès aujourd'hui !
type: docs
weight: 20
url: /fr/net/aspose.words.lists/listcollection/document/
---
## ListCollection.Document property

Obtient le document propriétaire.

```csharp
public DocumentBase Document { get; }
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

### Voir également

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [ListCollection](../)
* espace de noms [Aspose.Words.Lists](../../../aspose.words.lists/)
* Assemblée [Aspose.Words](../../../)
