---
title: ParagraphFormat.TabStops
linktitle: TabStops
articleTitle: TabStops
second_title: Aspose.Words per .NET
description: Scopri la proprietà ParagraphFormat TabStops per gestire facilmente le tabulazioni personalizzate, migliorando la formattazione del documento e la leggibilità.
type: docs
weight: 400
url: /it/net/aspose.words/paragraphformat/tabstops/
---
## ParagraphFormat.TabStops property

Ottiene la raccolta di tabulazioni personalizzate definite per questo oggetto.

```csharp
public TabStopCollection TabStops { get; }
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

* class [TabStopCollection](../../tabstopcollection/)
* class [ParagraphFormat](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
