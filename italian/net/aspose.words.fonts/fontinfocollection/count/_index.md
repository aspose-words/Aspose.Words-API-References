---
title: FontInfoCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words per .NET
description: Scopri la proprietà FontInfoCollection Count e recupera senza sforzo il numero totale di elementi nella tua raccolta per una gestione dei dati ottimale.
type: docs
weight: 10
url: /it/net/aspose.words.fonts/fontinfocollection/count/
---
## FontInfoCollection.Count property

Ottiene il numero di elementi contenuti nella raccolta.

```csharp
public int Count { get; }
```

## Esempi

Mostra informazioni sui font presenti nel documento vuoto.

```csharp
Document doc = new Document();

// Un documento vuoto contiene 3 font predefiniti. Ogni font nel documento
// avrà un oggetto FontInfo corrispondente che contiene dettagli su quel font.
Assert.AreEqual(3, doc.FontInfos.Count);

Assert.True(doc.FontInfos.Contains("Times New Roman"));
Assert.AreEqual(204, doc.FontInfos["Times New Roman"].Charset);

Assert.True(doc.FontInfos.Contains("Symbol"));
Assert.True(doc.FontInfos.Contains("Arial"));
```

### Guarda anche

* class [FontInfoCollection](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
