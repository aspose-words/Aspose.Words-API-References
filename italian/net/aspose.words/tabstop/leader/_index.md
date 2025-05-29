---
title: TabStop.Leader
linktitle: Leader
articleTitle: Leader
second_title: Aspose.Words per .NET
description: Scopri le proprietà di TabStop Leader per personalizzare i tipi di linea guida per le tue tabulazioni, migliorando la chiarezza e la presentazione dei tuoi documenti. Ottimizza la tua formattazione oggi stesso!
type: docs
weight: 40
url: /it/net/aspose.words/tabstop/leader/
---
## TabStop.Leader property

Ottiene o imposta il tipo di linea guida visualizzata sotto il carattere di tabulazione.

```csharp
public TabLeader Leader { get; set; }
```

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

* enum [TabLeader](../../tableader/)
* class [TabStop](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
