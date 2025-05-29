---
title: ListCollection.GetListByListId
linktitle: GetListByListId
articleTitle: GetListByListId
second_title: Aspose.Words für .NET
description: Rufen Sie Ihre gewünschte Liste mühelos mit der Methode GetListByListId ab. Greifen Sie mithilfe einer einfachen Listenkennung schnell auf Daten zu und steigern Sie so die Effizienz.
type: docs
weight: 80
url: /de/net/aspose.words.lists/listcollection/getlistbylistid/
---
## ListCollection.GetListByListId method

Ruft eine Liste anhand einer Listenkennung ab.

```csharp
public List GetListByListId(int listId)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| listId | Int32 | Die Listenkennung. |

### Rückgabewert

Gibt das Listenobjekt zurück. Gibt zurück`null` wenn eine Liste mit der angegebenen Kennung nicht gefunden wurde.

## Bemerkungen

Normalerweise brauchen Sie diese Methode nicht. Meistens wenden Sie die Listenformatierung auf Absätze an, indem Sie einfach die[`List`](../../listformat/list/) Eigenschaft des[`ListFormat`](../../listformat/) Objekt.

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

### Siehe auch

* class [List](../../list/)
* class [ListCollection](../)
* namensraum [Aspose.Words.Lists](../../../aspose.words.lists/)
* Montage [Aspose.Words](../../../)
