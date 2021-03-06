---
title: Document
second_title: Référence de l'API Aspose.Words pour .NET
description: Obtient le document propriétaire.
type: docs
weight: 10
url: /fr/net/aspose.words.lists/list/document/
---
## List.Document property

Obtient le document propriétaire.

```csharp
public DocumentBase Document { get; }
```

### Remarques

Une liste a toujours un document parent et n'est valide que dans le contexte de ce document.

### Exemples

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

* class [DocumentBase](../../../aspose.words/documentbase)
* class [List](../../list)
* espace de noms [Aspose.Words.Lists](../../list)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
