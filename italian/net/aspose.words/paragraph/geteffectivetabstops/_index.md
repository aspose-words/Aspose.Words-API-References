---
title: Paragraph.GetEffectiveTabStops
linktitle: GetEffectiveTabStops
articleTitle: GetEffectiveTabStops
second_title: Aspose.Words per .NET
description: Scopri il metodo GetEffectiveTabStops per recuperare tutte le tabulazioni in un paragrafo, comprese quelle provenienti da stili ed elenchi per una formattazione avanzata.
type: docs
weight: 270
url: /it/net/aspose.words/paragraph/geteffectivetabstops/
---
## Paragraph.GetEffectiveTabStops method

Restituisce una matrice di tutte le tabulazioni applicate a questo paragrafo, comprese quelle applicate indirettamente da stili o elenchi.

```csharp
public TabStop[] GetEffectiveTabStops()
```

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

* class [TabStop](../../tabstop/)
* class [Paragraph](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
