---
title: TabStop.Leader
second_title: Aspose.Words per .NET API Reference
description: TabStop proprietà. Ottiene o imposta il tipo di linea guida visualizzata sotto il carattere di tabulazione.
type: docs
weight: 40
url: /it/net/aspose.words/tabstop/leader/
---
## TabStop.Leader property

Ottiene o imposta il tipo di linea guida visualizzata sotto il carattere di tabulazione.

```csharp
public TabLeader Leader { get; set; }
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

* enum [TabLeader](../../tableader/)
* class [TabStop](../)
* spazio dei nomi [Aspose.Words](../../tabstop/)
* assemblea [Aspose.Words](../../../)


