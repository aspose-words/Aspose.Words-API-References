---
title: GetEffectiveTabStops
second_title: Aspose.Words per .NET API Reference
description: Restituisce larray di tutte le tabulazioni applicate a questo paragrafo incluse quelle applicate indirettamente da stili o elenchi.
type: docs
weight: 250
url: /it/net/aspose.words/paragraph/geteffectivetabstops/
---
## Paragraph.GetEffectiveTabStops method

Restituisce l'array di tutte le tabulazioni applicate a questo paragrafo, incluse quelle applicate indirettamente da stili o elenchi.

```csharp
public TabStop[] GetEffectiveTabStops()
```

### Esempi

Mostra come impostare punti di tabulazione personalizzati per un paragrafo.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Se ci troviamo in un paragrafo senza tabulazioni in questa raccolta,
// il cursore salterà di 36 punti ogni volta che premiamo il tasto Tab in Microsoft Word.
Assert.AreEqual(0, doc.FirstSection.Body.FirstParagraph.GetEffectiveTabStops().Length);

// Possiamo aggiungere tabulazioni personalizzate in Microsoft Word se abilitiamo il righello tramite la scheda "Visualizza".
// Ogni unità su questo righello è composta da due punti di tabulazione predefiniti, ovvero 72 punti.
// Possiamo aggiungere tabulazioni personalizzate a livello di codice in questo modo.
TabStopCollection tabStops = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.TabStops;
tabStops.Add(72, TabAlignment.Left, TabLeader.Dots);
tabStops.Add(216, TabAlignment.Center, TabLeader.Dashes);
tabStops.Add(360, TabAlignment.Right, TabLeader.Line);

// Possiamo vedere queste tabulazioni in Microsoft Word abilitando il righello tramite "Visualizza" -> "Mostra" -> "Governate".
Assert.AreEqual(3, para.GetEffectiveTabStops().Length);

// Tutti i caratteri di tabulazione che aggiungiamo utilizzeranno i punti di tabulazione sul righello e potrebbero,
// a seconda del valore del leader della scheda, lascia una linea tra le destinazioni di partenza e di arrivo della scheda.
para.AppendChild(new Run(doc, "\tTab 1\tTab 2\tTab 3"));

doc.Save(ArtifactsDir + "Paragraph.TabStops.docx");
```

### Guarda anche

* class [TabStop](../../tabstop)
* class [Paragraph](../../paragraph)
* spazio dei nomi [Aspose.Words](../../paragraph)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->