---
title: TabStopCollection.RemoveByPosition
linktitle: RemoveByPosition
articleTitle: RemoveByPosition
second_title: Aspose.Words per .NET
description: Rimuovi facilmente le tabulazioni dalla tua raccolta con il metodo RemoveByPosition. Semplifica la formattazione per un maggiore controllo sui documenti!
type: docs
weight: 120
url: /it/net/aspose.words/tabstopcollection/removebyposition/
---
## TabStopCollection.RemoveByPosition method

Rimuove una tabulazione nella posizione specificata dalla raccolta.

```csharp
public void RemoveByPosition(double position)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| position | Double | Posizione (in punti) della tabulazione da rimuovere. |

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

* class [TabStopCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
