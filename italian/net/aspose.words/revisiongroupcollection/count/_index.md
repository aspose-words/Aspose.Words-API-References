---
title: RevisionGroupCollection.Count
second_title: Aspose.Words per .NET API Reference
description: RevisionGroupCollection proprietà. Restituisce il numero di gruppi di revisione nella raccolta.
type: docs
weight: 10
url: /it/net/aspose.words/revisiongroupcollection/count/
---
## RevisionGroupCollection.Count property

Restituisce il numero di gruppi di revisione nella raccolta.

```csharp
public int Count { get; }
```

### Esempi

Mostra come stampare informazioni su un gruppo di revisioni in un documento.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

Assert.AreEqual(7, doc.Revisions.Groups.Count);

foreach (RevisionGroup group in doc.Revisions.Groups)
{
    Console.WriteLine(
        $"Revision author: {group.Author}; Revision type: {group.RevisionType} \n\tRevision text: {group.Text}");
}
```

### Guarda anche

* class [RevisionGroupCollection](../)
* spazio dei nomi [Aspose.Words](../../revisiongroupcollection/)
* assemblea [Aspose.Words](../../../)


