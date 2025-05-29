---
title: TabAlignment Enum
linktitle: TabAlignment
articleTitle: TabAlignment
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.TabAlignment per l'allineamento personalizzabile delle tabulazioni. Migliora la formattazione dei documenti con precisione e flessibilità oggi stesso!
type: docs
weight: 7030
url: /it/net/aspose.words/tabalignment/
---
## TabAlignment enumeration

Specifica l'allineamento/tipo di una tabulazione.

```csharp
public enum TabAlignment
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Left | `0` | Allinea a sinistra il testo dopo la tabulazione. |
| Center | `1` | Centra il testo attorno alla tabulazione. |
| Right | `2` | Allinea a destra il testo alla tabulazione. |
| Decimal | `3` | Allinea il testo al punto decimale. |
| Bar | `4` | Disegna una barra verticale nella posizione di tabulazione. |
| List | `6` | La tabulazione è un delimitatore tra il numero/punto elenco e il testo in una voce di elenco. |
| Clear | `7` | Cancella qualsiasi tabulazione in questa posizione. |

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
