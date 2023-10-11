---
title: Class TabStop
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.TabStop classe. Rappresenta una singola tabulazione personalizzata. ILTabStoploggetto è un membro di the TabStopCollection collezione.
type: docs
weight: 6200
url: /it/net/aspose.words/tabstop/
---
## TabStop class

Rappresenta una singola tabulazione personalizzata. IL`TabStop`l'oggetto è un membro di the [`TabStopCollection`](../tabstopcollection/) collezione.

Per saperne di più, visita il[Modello oggetto documento Aspose.Words (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) articolo di documentazione.

```csharp
public sealed class TabStop
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [TabStop](tabstop/#constructor)(double) | Inizializza una nuova istanza di questa classe. |
| [TabStop](tabstop/#constructor_1)(double, TabAlignment, TabLeader) | Inizializza una nuova istanza di questa classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Alignment](../../aspose.words/tabstop/alignment/) { get; set; } | Ottiene o imposta l'allineamento del testo in questa tabulazione. |
| [IsClear](../../aspose.words/tabstop/isclear/) { get; } | Restituisce`VERO` se questo punto di tabulazione cancella eventuali punti di tabulazione esistenti in questa posizione. |
| [Leader](../../aspose.words/tabstop/leader/) { get; set; } | Ottiene o imposta il tipo di linea guida visualizzata sotto il carattere di tabulazione. |
| [Position](../../aspose.words/tabstop/position/) { get; } | Ottiene la posizione del punto di tabulazione in punti. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Equals](../../aspose.words/tabstop/equals/#equals)(TabStop) | Confronta con quanto specificato`TabStop` . |
| override [GetHashCode](../../aspose.words/tabstop/gethashcode/)() | Calcola il codice hash per questo oggetto. |

### Osservazioni

Normalmente, un punto di tabulazione specifica una posizione in cui esiste un punto di tabulazione. Ma poiché i punti di tabulazione possono essere ereditati dagli stili principali, potrebbe essere necessario che l'oggetto figlio definisca esplicitamente che non ci sono punti di tabulazione in una determinata posizione. Per cancellare una tabulazione ereditata in una determinata posizione, crea un file`TabStop` oggetto e set [`Alignment`](./alignment/) AClear.

Per ulteriori informazioni, vedere[`TabStopCollection`](../tabstopcollection/).

### Esempi

Mostra come modificare la posizione della tabulazione destra nei paragrafi relativi al sommario.

```csharp
Document doc = new Document(MyDir + "Table of contents.docx");

// Scorrere tutti i paragrafi con stili basati sui risultati del sommario; questo è qualsiasi stile compreso tra TOC e TOC9.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
    if (para.ParagraphFormat.Style.StyleIdentifier >= StyleIdentifier.Toc1 &&
        para.ParagraphFormat.Style.StyleIdentifier <= StyleIdentifier.Toc9)
    {
        // Ottieni la prima scheda utilizzata in questo paragrafo, dovrebbe essere la scheda utilizzata per allineare i numeri di pagina.
        TabStop tab = para.ParagraphFormat.TabStops[0];

        // Sostituisce la prima tabulazione predefinita, interrompendola con una tabulazione personalizzata.
        para.ParagraphFormat.TabStops.RemoveByPosition(tab.Position);
        para.ParagraphFormat.TabStops.Add(tab.Position - 50, tab.Alignment, tab.Leader);
    }

doc.Save(ArtifactsDir + "Styles.ChangeTocsTabStops.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)


