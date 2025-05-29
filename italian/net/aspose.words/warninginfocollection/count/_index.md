---
title: WarningInfoCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words per .NET
description: Scopri la proprietà WarningInfoCollection Count per accedere facilmente al numero totale di elementi nella tua raccolta per una gestione efficiente dei dati.
type: docs
weight: 20
url: /it/net/aspose.words/warninginfocollection/count/
---
## WarningInfoCollection.Count property

Ottiene il numero di elementi contenuti nella raccolta.

```csharp
public int Count { get; }
```

## Esempi

Mostra come ricevere avvisi sui formati non supportati.

```csharp
WarningInfoCollection warnings = new WarningInfoCollection();
Document doc = new Document(MyDir + "FB2 document.fb2", new LoadOptions { WarningCallback = warnings });

Assert.AreEqual("The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document.", warnings[0].Description);
Assert.AreEqual(1, warnings.Count);
```

### Guarda anche

* class [WarningInfoCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
