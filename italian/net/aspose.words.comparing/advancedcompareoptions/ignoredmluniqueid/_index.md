---
title: AdvancedCompareOptions.IgnoreDmlUniqueId
linktitle: IgnoreDmlUniqueId
articleTitle: IgnoreDmlUniqueId
second_title: Aspose.Words per .NET
description: Scopri la proprietà IgnoreDmlUniqueId di AdvancedCompareOptions per migliorare l'elaborazione di DrawingML gestendo in modo efficiente gli ID univoci. Ottimizza il tuo flusso di lavoro!
type: docs
weight: 20
url: /it/net/aspose.words.comparing/advancedcompareoptions/ignoredmluniqueid/
---
## AdvancedCompareOptions.IgnoreDmlUniqueId property

Specifica se ignorare la differenza nell'ID univoco di DrawingML.

```csharp
public bool IgnoreDmlUniqueId { get; set; }
```

## Osservazioni

Il valore predefinito è`falso` .

## Esempi

Mostra come confrontare i documenti ignorando l'ID univoco DML.

```csharp
Document docA = new Document(MyDir + "DML unique ID original.docx");
Document docB = new Document(MyDir + "DML unique ID compare.docx");

// Per impostazione predefinita, Aspose.Words non ignora l'ID univoco di DML e il conteggio delle revisioni era 2.
// Se ignoriamo l'ID univoco di DML e il conteggio delle revisioni è 0.
CompareOptions compareOptions = new CompareOptions();
compareOptions.AdvancedOptions.IgnoreDmlUniqueId = isIgnoreDmlUniqueId;

docA.Compare(docB, "Aspose.Words", DateTime.Now, compareOptions);

Assert.AreEqual(isIgnoreDmlUniqueId ? 0 : 2, docA.Revisions.Count);
```

### Guarda anche

* class [AdvancedCompareOptions](../)
* spazio dei nomi [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* assemblea [Aspose.Words](../../../)
