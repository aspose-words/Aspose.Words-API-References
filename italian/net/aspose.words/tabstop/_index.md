---
title: TabStop Class
linktitle: TabStop
articleTitle: TabStop
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.TabStop, la soluzione per tabulazioni personalizzate nella formattazione dei documenti. Migliora i tuoi documenti con precisione e semplicità!
type: docs
weight: 7050
url: /it/net/aspose.words/tabstop/
---
## TabStop class

Rappresenta una singola tabulazione personalizzata.`TabStop` l'oggetto è un membro di the [`TabStopCollection`](../tabstopcollection/) collezione.

Per saperne di più, visita il[Modello a oggetti del documento (DOM) di Aspose.Words](https://docs.aspose.com/words/net/aspose-words-document-object-model/) articolo di documentazione.

```csharp
public sealed class TabStop
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [TabStop](tabstop/#constructor)(*double*) | Inizializza una nuova istanza di questa classe. |
| [TabStop](tabstop/#constructor_1)(*double, [TabAlignment](../tabalignment/), [TabLeader](../tableader/)*) | Inizializza una nuova istanza di questa classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Alignment](../../aspose.words/tabstop/alignment/) { get; set; } | Ottiene o imposta l'allineamento del testo in questa tabulazione. |
| [IsClear](../../aspose.words/tabstop/isclear/) { get; } | Restituisce`VERO` se questa tabulazione cancella tutte le tabulazioni esistenti in questa posizione. |
| [Leader](../../aspose.words/tabstop/leader/) { get; set; } | Ottiene o imposta il tipo di linea guida visualizzata sotto il carattere di tabulazione. |
| [Position](../../aspose.words/tabstop/position/) { get; } | Ottiene la posizione della tabulazione in punti. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Equals](../../aspose.words/tabstop/equals/#equals)(*TabStop*) | Confronta con lo specificato`TabStop` . |
| override [GetHashCode](../../aspose.words/tabstop/gethashcode/)() | Calcola il codice hash per questo oggetto. |

## Osservazioni

Normalmente, una tabulazione specifica una posizione in cui è presente una tabulazione. Tuttavia, poiché le tabulazioni possono essere ereditate dagli stili padre, potrebbe essere necessario che l'oggetto figlio definisca esplicitamente che non vi è alcuna tabulazione in una determinata posizione. Per cancellare una tabulazione ereditata in una determinata posizione, creare un`TabStop` oggetto e set [`Alignment`](./alignment/) AClear.

Per maggiori informazioni vedere[`TabStopCollection`](../tabstopcollection/).

## Esempi

Mostra come modificare la posizione della tabulazione destra nei paragrafi relativi all'indice.

```csharp
Document doc = new Document(MyDir + "Table of contents.docx");

// Scorrere tutti i paragrafi con stili basati sui risultati dell'indice; questo è qualsiasi stile compreso tra TOC e TOC9.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
    if (para.ParagraphFormat.Style.StyleIdentifier >= StyleIdentifier.Toc1 &&
        para.ParagraphFormat.Style.StyleIdentifier <= StyleIdentifier.Toc9)
    {
        // Ottieni la prima tabulazione utilizzata in questo paragrafo. Dovrebbe essere la tabulazione utilizzata per allineare i numeri di pagina.
        TabStop tab = para.ParagraphFormat.TabStops[0];

        // Sostituisci la prima tabulazione predefinita con una tabulazione personalizzata.
        para.ParagraphFormat.TabStops.RemoveByPosition(tab.Position);
        para.ParagraphFormat.TabStops.Add(tab.Position - 50, tab.Alignment, tab.Leader);
    }

doc.Save(ArtifactsDir + "Styles.ChangeTocsTabStops.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
