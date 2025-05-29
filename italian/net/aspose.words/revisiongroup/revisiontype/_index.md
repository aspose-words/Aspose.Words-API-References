---
title: RevisionGroup.RevisionType
linktitle: RevisionType
articleTitle: RevisionType
second_title: Aspose.Words per .NET
description: Scopri la proprietà RevisionType di RevisionGroup per identificare e gestire facilmente i tipi di revisione nel tuo progetto. Semplifica il tuo flusso di lavoro oggi stesso!
type: docs
weight: 20
url: /it/net/aspose.words/revisiongroup/revisiontype/
---
## RevisionGroup.RevisionType property

Ottiene il tipo di revisioni incluse in questo gruppo.

```csharp
public RevisionType RevisionType { get; }
```

## Esempi

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

* enum [RevisionType](../../revisiontype/)
* class [RevisionGroup](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
