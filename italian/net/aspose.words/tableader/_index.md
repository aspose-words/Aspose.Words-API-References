---
title: TabLeader Enum
linktitle: TabLeader
articleTitle: TabLeader
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.TabLeader, che definisce gli stili delle linee guida per le schede, migliorando la formattazione dei documenti e la leggibilità nei tuoi progetti.
type: docs
weight: 7040
url: /it/net/aspose.words/tableader/
---
## TabLeader enumeration

Specifica il tipo di linea guida visualizzata sotto il carattere di tabulazione.

```csharp
public enum TabLeader
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | Non viene visualizzata alcuna linea guida. |
| Dots | `1` | La linea guida è composta da punti. |
| Dashes | `2` | La linea guida è composta da trattini. |
| Line | `3` | La linea guida è una linea singola. |
| Heavy | `4` | La linea guida è una singola linea spessa. |
| MiddleDot | `5` | La linea guida è composta da punti centrali. |

## Esempi

Mostra come impostare tabulazioni personalizzate per un paragrafo.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Se ci troviamo in un paragrafo senza tabulazioni in questa raccolta,
// il cursore salterà di 36 punti ogni volta che premiamo il tasto Tab in Microsoft Word.
Assert.AreEqual(0, doc.FirstSection.Body.FirstParagraph.GetEffectiveTabStops().Length);

// Possiamo aggiungere tabulazioni personalizzate in Microsoft Word se abilitiamo il righello tramite la scheda "Visualizza".
// Ogni unità su questo righello è costituita da due tabulazioni predefinite, ovvero 72 punti.
// Possiamo aggiungere tabulazioni personalizzate tramite programmazione in questo modo.
TabStopCollection tabStops = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.TabStops;
tabStops.Add(72, TabAlignment.Left, TabLeader.Dots);
tabStops.Add(216, TabAlignment.Center, TabLeader.Dashes);
tabStops.Add(360, TabAlignment.Right, TabLeader.Line);

// Possiamo vedere queste tabulazioni in Microsoft Word abilitando il righello tramite "Visualizza" -> "Mostra" -> "Righello".
Assert.AreEqual(3, para.GetEffectiveTabStops().Length);

// Tutti i caratteri di tabulazione che aggiungiamo utilizzeranno le tabulazioni sul righello e potrebbero,
// a seconda del valore del leader della tabulazione, lasciare una riga tra le destinazioni di partenza e di arrivo della tabulazione.
para.AppendChild(new Run(doc, "\tTab 1\tTab 2\tTab 3"));

doc.Save(ArtifactsDir + "Paragraph.TabStops.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
