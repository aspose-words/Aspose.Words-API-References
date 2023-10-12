---
title: Class RevisionGroupCollection
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.RevisionGroupCollection classe. Una raccolta diRevisionGroup oggetti che rappresentano i gruppi di revisione nel documento.
type: docs
weight: 4790
url: /it/net/aspose.words/revisiongroupcollection/
---
## RevisionGroupCollection class

Una raccolta di[`RevisionGroup`](../revisiongroup/) oggetti che rappresentano i gruppi di revisione nel documento.

Per saperne di più, visita il[Tieni traccia delle modifiche in un documento](https://docs.aspose.com/words/net/track-changes-in-a-document/) articolo di documentazione.

```csharp
public sealed class RevisionGroupCollection : IEnumerable<RevisionGroup>
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words/revisiongroupcollection/count/) { get; } | Restituisce il numero di gruppi di revisione nella raccolta. |
| [Item](../../aspose.words/revisiongroupcollection/item/) { get; } | Restituisce un gruppo di revisione all'indice specificato. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetEnumerator](../../aspose.words/revisiongroupcollection/getenumerator/)() | Restituisce un oggetto enumeratore. |

### Osservazioni

Non crei direttamente istanze di questa classe. Usa il[`Groups`](../revisioncollection/groups/) per ottenere i gruppi di revisione presenti in un documento.

### Esempi

Mostra come ottenere un gruppo di revisioni in un documento.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

RevisionGroup revisionGroup = doc.Revisions.Groups[0];
```

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

* class [RevisionGroup](../revisiongroup/)
* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)


