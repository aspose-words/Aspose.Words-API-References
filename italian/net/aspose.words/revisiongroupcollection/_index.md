---
title: RevisionGroupCollection Class
linktitle: RevisionGroupCollection
articleTitle: RevisionGroupCollection
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.RevisionGroupCollection, che offre una gestione efficiente dei gruppi di revisione dei documenti per una modifica e una collaborazione migliorate.
type: docs
weight: 5530
url: /it/net/aspose.words/revisiongroupcollection/
---
## RevisionGroupCollection class

Una raccolta di[`RevisionGroup`](../revisiongroup/)oggetti che rappresentano gruppi di revisione nel documento.

Per saperne di più, visita il[Traccia le modifiche in un documento](https://docs.aspose.com/words/net/track-changes-in-a-document/) articolo di documentazione.

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

## Osservazioni

Non creare istanze di questa classe direttamente. Utilizzare il[`Groups`](../revisioncollection/groups/) Proprietà per ottenere i gruppi di revisione presenti in un documento.

## Esempi

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
