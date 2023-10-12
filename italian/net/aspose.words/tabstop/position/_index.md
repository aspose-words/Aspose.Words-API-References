---
title: TabStop.Position
second_title: Aspose.Words per .NET API Reference
description: TabStop proprietà. Ottiene la posizione del punto di tabulazione in punti.
type: docs
weight: 50
url: /it/net/aspose.words/tabstop/position/
---
## TabStop.Position property

Ottiene la posizione del punto di tabulazione in punti.

```csharp
public double Position { get; }
```

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

* class [TabStop](../)
* spazio dei nomi [Aspose.Words](../../tabstop/)
* assemblea [Aspose.Words](../../../)


