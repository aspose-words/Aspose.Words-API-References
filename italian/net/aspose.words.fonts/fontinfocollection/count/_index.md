---
title: FontInfoCollection.Count
second_title: Aspose.Words per .NET API Reference
description: FontInfoCollection proprietà. Ottiene il numero di elementi contenuti nella raccolta.
type: docs
weight: 10
url: /it/net/aspose.words.fonts/fontinfocollection/count/
---
## FontInfoCollection.Count property

Ottiene il numero di elementi contenuti nella raccolta.

```csharp
public int Count { get; }
```

### Esempi

Mostra informazioni sui caratteri presenti nel documento vuoto.

```csharp
Document doc = new Document();

// Un documento vuoto contiene 3 caratteri predefiniti. Ogni carattere nel documento
// avrà un oggetto FontInfo corrispondente che contiene dettagli su quel carattere.
Assert.AreEqual(3, doc.FontInfos.Count);

Assert.True(doc.FontInfos.Contains("Times New Roman"));
Assert.AreEqual(204, doc.FontInfos["Times New Roman"].Charset);

Assert.True(doc.FontInfos.Contains("Symbol"));
Assert.True(doc.FontInfos.Contains("Arial"));
```

### Guarda anche

* class [FontInfoCollection](../)
* spazio dei nomi [Aspose.Words.Fonts](../../fontinfocollection/)
* assemblea [Aspose.Words](../../../)


