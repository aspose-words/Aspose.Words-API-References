---
title: List.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie Dokumenteigenschaften auflisten und mühelos auf Eigentümerdetails zugreifen. Entfesseln Sie noch heute Ihr Dokumentenmanagement-Potenzial!
type: docs
weight: 10
url: /de/net/aspose.words.lists/list/document/
---
## List.Document property

Ruft das Besitzerdokument ab.

```csharp
public DocumentBase Document { get; }
```

## Bemerkungen

Eine Liste hat immer ein übergeordnetes Dokument und ist nur im Kontext dieses Dokuments gültig.

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

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [List](../)
* namensraum [Aspose.Words.Lists](../../../aspose.words.lists/)
* Montage [Aspose.Words](../../../)
