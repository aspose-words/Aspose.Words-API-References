---
title: WarningInfoCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words per .NET
description: Accedi facilmente a specifici elementi di WarningInfoCollection tramite indice. Semplifica la gestione dei dati con la nostra intuitiva funzionalità di gestione delle proprietà!
type: docs
weight: 30
url: /it/net/aspose.words/warninginfocollection/item/
---
## WarningInfoCollection indexer

Ottiene un elemento all'indice specificato.

```csharp
public WarningInfo this[int index] { get; }
```

| Parametro | Descrizione |
| --- | --- |
| index | Indice basato su zero dell'elemento. |

## Esempi

Mostra come ricevere avvisi sui formati non supportati.

```csharp
WarningInfoCollection warnings = new WarningInfoCollection();
Document doc = new Document(MyDir + "FB2 document.fb2", new LoadOptions { WarningCallback = warnings });

Assert.AreEqual("The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document.", warnings[0].Description);
Assert.AreEqual(1, warnings.Count);
```

### Guarda anche

* class [WarningInfo](../../warninginfo/)
* class [WarningInfoCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
