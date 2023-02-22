---
title: RevisionGroup.Author
second_title: Aspose.Words per .NET API Reference
description: RevisionGroup proprietà. Ottiene lautore di questo gruppo di revisioni.
type: docs
weight: 10
url: /it/net/aspose.words/revisiongroup/author/
---
## RevisionGroup.Author property

Ottiene l'autore di questo gruppo di revisioni.

```csharp
public string Author { get; }
```

### Esempi

Mostra come stampare le informazioni su un gruppo di revisioni in un documento.

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

* class [RevisionGroup](../)
* spazio dei nomi [Aspose.Words](../../revisiongroup/)
* assemblea [Aspose.Words](../../../)


