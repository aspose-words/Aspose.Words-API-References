---
title: List.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words pour .NET
description: Découvrez comment répertorier les propriétés de vos documents et accéder facilement aux informations de propriété. Libérez dès aujourd'hui votre potentiel en matière de gestion documentaire !
type: docs
weight: 10
url: /fr/net/aspose.words.lists/list/document/
---
## List.Document property

Obtient le document propriétaire.

```csharp
public DocumentBase Document { get; }
```

## Remarques

Une liste a toujours un document parent et n'est valide que dans le contexte de ce document.

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
* class [List](../)
* espace de noms [Aspose.Words.Lists](../../../aspose.words.lists/)
* Assemblée [Aspose.Words](../../../)
