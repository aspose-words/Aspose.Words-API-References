---
title: CompareOptions.AdvancedOptions
linktitle: AdvancedOptions
articleTitle: AdvancedOptions
second_title: Aspose.Words per .NET
description: Scopri CompareOptions AdvancedOptions per migliorare i tuoi confronti. Ottieni risultati precisi con impostazioni personalizzate per un output ottimale.
type: docs
weight: 20
url: /it/net/aspose.words.comparing/compareoptions/advancedoptions/
---
## CompareOptions.AdvancedOptions property

Specifica opzioni di confronto avanzate che potrebbero aiutare a produrre un output di confronto più preciso.

```csharp
public AdvancedCompareOptions AdvancedOptions { get; }
```

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

* class [AdvancedCompareOptions](../../advancedcompareoptions/)
* class [CompareOptions](../)
* spazio dei nomi [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* assemblea [Aspose.Words](../../../)
