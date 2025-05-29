---
title: Style.StyleIdentifier
linktitle: StyleIdentifier
articleTitle: StyleIdentifier
second_title: Aspose.Words per .NET
description: Scopri la proprietà StyleIdentifier, indipendente dalle impostazioni locali, per gli stili predefiniti. Migliora i tuoi progetti con soluzioni di stile coerenti e versatili.
type: docs
weight: 180
url: /it/net/aspose.words/style/styleidentifier/
---
## Style.StyleIdentifier property

Ottiene l'identificatore di stile indipendente dalle impostazioni locali per uno stile incorporato.

```csharp
public StyleIdentifier StyleIdentifier { get; }
```

## Osservazioni

Per gli stili definiti dall'utente (personalizzati), questa proprietà restituisceUser.

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

* enum [StyleIdentifier](../../styleidentifier/)
* class [Style](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
