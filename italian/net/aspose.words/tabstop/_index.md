---
title: Class TabStop
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.TabStop classe. Rappresenta una singola tabulazione personalizzata. Il TabStop loggetto è un membro di TabStopCollection raccolta.
type: docs
weight: 5900
url: /it/net/aspose.words/tabstop/
---
## TabStop class

Rappresenta una singola tabulazione personalizzata. Il **TabStop** l'oggetto è un membro di [`TabStopCollection`](../tabstopcollection/) raccolta.

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
| [Alignment](../../aspose.words/tabstop/alignment/) { get; set; } | Ottiene o imposta l'allineamento del testo a questo punto di tabulazione. |
| [IsClear](../../aspose.words/tabstop/isclear/) { get; } | Restituisce vero se questa tabulazione cancella eventuali tabulazioni esistenti in questa posizione. |
| [Leader](../../aspose.words/tabstop/leader/) { get; set; } | Ottiene o imposta il tipo della linea guida visualizzata sotto il carattere di tabulazione. |
| [Position](../../aspose.words/tabstop/position/) { get; } | Ottiene la posizione del punto di tabulazione in punti. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Equals](../../aspose.words/tabstop/equals/#equals)(TabStop) | Confronta con TabStop specificato. |
| override [GetHashCode](../../aspose.words/tabstop/gethashcode/)() | Calcola il codice hash per questo oggetto. |

### Osservazioni

Normalmente, una tabulazione specifica una posizione in cui esiste una tabulazione. Ma poiché i punti di tabulazione possono essere ereditati dagli stili padre, potrebbe essere necessario che l'oggetto figlio definisca esplicitamente che non vi è alcun punto di tabulazione in una determinata posizione. Per cancellare una tabulazione ereditata in una determinata posizione, creare a **TabStop** oggetto e set [`Alignment`](./alignment/) a`TabAlignment.Cancella`.

Per ulteriori informazioni, vedere[`TabStopCollection`](../tabstopcollection/).

### Esempi

Mostra come modificare la posizione della tabulazione destra nei paragrafi relativi al sommario.

```csharp
Document doc = new Document(MyDir + "Table of contents.docx");

// Scorri tutti i paragrafi con stili basati sui risultati del sommario; questo è qualsiasi stile tra TOC e TOC9.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
    if (para.ParagraphFormat.Style.StyleIdentifier >= StyleIdentifier.Toc1 &&
        para.ParagraphFormat.Style.StyleIdentifier <= StyleIdentifier.Toc9)
    {
        // Ottieni la prima scheda utilizzata in questo paragrafo, questa dovrebbe essere la scheda utilizzata per allineare i numeri di pagina.
        TabStop tab = para.ParagraphFormat.TabStops[0];

        // Sostituisci la prima tabulazione predefinita, ferma con una tabulazione personalizzata.
        para.ParagraphFormat.TabStops.RemoveByPosition(tab.Position);
        para.ParagraphFormat.TabStops.Add(tab.Position - 50, tab.Alignment, tab.Leader);
    }

doc.Save(ArtifactsDir + "Styles.ChangeTocsTabStops.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)


