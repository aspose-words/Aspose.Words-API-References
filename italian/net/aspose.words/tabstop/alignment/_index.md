---
title: TabStop.Alignment
linktitle: Alignment
articleTitle: Alignment
second_title: Aspose.Words per .NET
description: Scopri la proprietà Allineamento TabStop per personalizzare facilmente l'allineamento del testo in corrispondenza delle tabulazioni, migliorando così il layout e la leggibilità del tuo documento.
type: docs
weight: 20
url: /it/net/aspose.words/tabstop/alignment/
---
## TabStop.Alignment property

Ottiene o imposta l'allineamento del testo in questa tabulazione.

```csharp
public TabAlignment Alignment { get; set; }
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

* enum [TabAlignment](../../tabalignment/)
* class [TabStop](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
