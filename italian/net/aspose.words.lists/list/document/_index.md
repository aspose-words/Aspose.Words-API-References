---
title: List.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words per .NET
description: Scopri come elencare le proprietà dei documenti e accedere ai dettagli di proprietà senza sforzo. Sfrutta subito il tuo potenziale di gestione documentale!
type: docs
weight: 10
url: /it/net/aspose.words.lists/list/document/
---
## List.Document property

Ottiene il documento del proprietario.

```csharp
public DocumentBase Document { get; }
```

## Osservazioni

Un elenco ha sempre un documento padre ed è valido solo nel contesto di quel documento.

## Esempi

Mostra come verificare le proprietà dei documenti proprietari degli elenchi.

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

### Guarda anche

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [List](../)
* spazio dei nomi [Aspose.Words.Lists](../../../aspose.words.lists/)
* assemblea [Aspose.Words](../../../)
