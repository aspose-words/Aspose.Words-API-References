---
title: RevisionGroup.Text
second_title: Aspose.Words per .NET API Reference
description: RevisionGroup proprietà. Restituisce il testo inserito/eliminato/spostato o la descrizione del cambio formato.
type: docs
weight: 30
url: /it/net/aspose.words/revisiongroup/text/
---
## RevisionGroup.Text property

Restituisce il testo inserito/eliminato/spostato o la descrizione del cambio formato.

```csharp
public string Text { get; }
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

* class [RevisionGroup](../)
* spazio dei nomi [Aspose.Words](../../revisiongroup/)
* assemblea [Aspose.Words](../../../)


