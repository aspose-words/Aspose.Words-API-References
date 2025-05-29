---
title: SectionCollection Class
linktitle: SectionCollection
articleTitle: SectionCollection
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.SectionCollection: la soluzione ideale per gestire in modo efficiente le sezioni dei documenti, con funzionalità potenti e flessibilità.
type: docs
weight: 6570
url: /it/net/aspose.words/sectioncollection/
---
## SectionCollection class

Una raccolta di[`Section`](../section/) oggetti nel documento.

Per saperne di più, visita il[Lavorare con le sezioni](https://docs.aspose.com/words/net/working-with-sections/) articolo di documentazione.

```csharp
public class SectionCollection : NodeCollection
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Ottiene il numero di nodi nella raccolta. |
| [Item](../../aspose.words/sectioncollection/item/) { get; } | Recupera una sezione all'indice specificato. (2 indexers) |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | Aggiunge un nodo alla fine della raccolta. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Rimuove tutti i nodi da questa raccolta e dal documento. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | Determina se un nodo è nella raccolta. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Fornisce una semplice iterazione in stile "foreach" sulla raccolta di nodi. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | Restituisce l'indice basato su zero del nodo specificato. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | Inserisce un nodo nella raccolta all'indice specificato. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | Rimuove il nodo dalla raccolta e dal documento. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Rimuove il nodo all'indice specificato dalla raccolta e dal documento. |
| [ToArray](../../aspose.words/sectioncollection/toarray/#toarray_1)() | Copia tutte le sezioni dalla raccolta in un nuovo array di sezioni. (2 methods) |

## Osservazioni

Un documento di Microsoft Word può contenere più sezioni. Per creare una sezione in un documento di Microsoft Word, seleziona il comando Inserisci/Interruzione e seleziona un tipo di interruzione. L'interruzione specifica se la sezione inizia su una nuova pagina o sulla stessa pagina.

L'inserimento e la rimozione di sezioni a livello di codice possono essere utilizzati per personalizzare i documenti prodotti durante la stampa unione. Se un documento deve avere contenuti o parti di contenuto diversi in base a determinati criteri, è possibile creare un documento "master" contenente più sezioni ed eliminarne alcune prima o dopo la stampa unione.

## Esempi

Mostra come aggiungere e rimuovere sezioni in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

Assert.AreEqual("Section 1\x000cSection 2", doc.GetText().Trim());

// Elimina la prima sezione dal documento.
doc.Sections.RemoveAt(0);

Assert.AreEqual("Section 2", doc.GetText().Trim());

// Aggiungere una copia di quella che ora è la prima sezione alla fine del documento.
int lastSectionIdx = doc.Sections.Count - 1;
Section newSection = doc.Sections[lastSectionIdx].Clone();
doc.Sections.Add(newSection);

Assert.AreEqual("Section 2\x000cSection 2", doc.GetText().Trim());
```

### Guarda anche

* class [NodeCollection](../nodecollection/)
* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
