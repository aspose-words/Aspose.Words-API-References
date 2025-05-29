---
title: ListCollection.GetListByListId
linktitle: GetListByListId
articleTitle: GetListByListId
second_title: Aspose.Words pour .NET
description: Récupérez facilement la liste souhaitée grâce à la méthode GetListByListId. Accédez rapidement aux données grâce à un identifiant de liste simple pour une efficacité accrue.
type: docs
weight: 80
url: /fr/net/aspose.words.lists/listcollection/getlistbylistid/
---
## ListCollection.GetListByListId method

Obtient une liste par un identifiant de liste.

```csharp
public List GetListByListId(int listId)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| listId | Int32 | L'identifiant de la liste. |

### Return_Value

Renvoie l'objet liste.`nul` si aucune liste avec l'identifiant spécifié n'a été trouvée.

## Remarques

Vous n'avez généralement pas besoin d'utiliser cette méthode. La plupart du temps, vous appliquez le formatage de liste aux paragraphes simplement en définissant le[`List`](../../listformat/list/) propriété du[`ListFormat`](../../listformat/) objet.

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

* class [List](../../list/)
* class [ListCollection](../)
* espace de noms [Aspose.Words.Lists](../../../aspose.words.lists/)
* Assemblée [Aspose.Words](../../../)
