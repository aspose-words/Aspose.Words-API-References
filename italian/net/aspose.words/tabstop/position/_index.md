---
title: TabStop.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words per .NET
description: Scopri la proprietà TabStop Position per trovare facilmente le posizioni delle tabulazioni nei punti, migliorando la precisione del layout e l'efficienza della progettazione.
type: docs
weight: 50
url: /it/net/aspose.words/tabstop/position/
---
## TabStop.Position property

Ottiene la posizione della tabulazione in punti.

```csharp
public double Position { get; }
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

* class [TabStop](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
