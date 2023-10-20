---
title: Paragraph.GetEffectiveTabStops
linktitle: GetEffectiveTabStops
articleTitle: GetEffectiveTabStops
second_title: Aspose.Words per .NET
description: Paragraph GetEffectiveTabStops metodo. Restituisce larray di tutti i punti di tabulazione applicati a questo paragrafo inclusi quelli applicati indirettamente da stili o elenchi in C#.
type: docs
weight: 250
url: /it/net/aspose.words/paragraph/geteffectivetabstops/
---
## Paragraph.GetEffectiveTabStops method

Restituisce l'array di tutti i punti di tabulazione applicati a questo paragrafo, inclusi quelli applicati indirettamente da stili o elenchi.

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
// Ogni unità su questo righello corrisponde a due tabulazioni predefinite, ovvero 72 punti.
// Possiamo aggiungere tabulazioni personalizzate a livello di codice in questo modo.
TabStopCollection tabStops = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.TabStops;
tabStops.Add(72, TabAlignment.Left, TabLeader.Dots);
tabStops.Add(216, TabAlignment.Center, TabLeader.Dashes);
tabStops.Add(360, TabAlignment.Right, TabLeader.Line);

// Possiamo vedere questi punti di tabulazione in Microsoft Word abilitando il righello tramite "Visualizza" -> "Mostra" -> "Governate".
Assert.AreEqual(3, para.GetEffectiveTabStops().Length);

// Qualsiasi carattere di tabulazione aggiunto utilizzerà i punti di tabulazione sul righello e potrebbe,
// a seconda del valore del leader della scheda, lascia una linea tra le destinazioni di partenza e di arrivo della scheda.
para.AppendChild(new Run(doc, "\tTab 1\tTab 2\tTab 3"));

doc.Save(ArtifactsDir + "Paragraph.TabStops.docx");
```

### Guarda anche

* class [TabStop](../../tabstop/)
* class [Paragraph](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
