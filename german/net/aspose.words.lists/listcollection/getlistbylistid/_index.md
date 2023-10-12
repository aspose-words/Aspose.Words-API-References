---
title: ListCollection.GetListByListId
second_title: Aspose.Words für .NET-API-Referenz
description: ListCollection methode. Ruft eine Liste anhand einer Listenkennung ab.
type: docs
weight: 70
url: /de/net/aspose.words.lists/listcollection/getlistbylistid/
---
## ListCollection.GetListByListId method

Ruft eine Liste anhand einer Listenkennung ab.

```csharp
public List GetListByListId(int listId)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| listId | Int32 | Der Listenbezeichner. |

### Rückgabewert

Gibt das Listenobjekt zurück. Kehrt zurück`Null` wenn keine Liste mit der angegebenen Kennung gefunden wurde.

### Bemerkungen

Normalerweise müssen Sie diese Methode nicht verwenden. Meistens wenden Sie die Listenformatierung auf Absätze an, indem Sie einfach die festlegen[`List`](../../listformat/list/) property des[`ListFormat`](../../listformat/) Objekt.

### Beispiele

Zeigt, wie Besitzerdokumenteigenschaften von Listen überprüft werden.

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

### Siehe auch

* class [List](../../list/)
* class [ListCollection](../)
* namensraum [Aspose.Words.Lists](../../listcollection/)
* Montage [Aspose.Words](../../../)


