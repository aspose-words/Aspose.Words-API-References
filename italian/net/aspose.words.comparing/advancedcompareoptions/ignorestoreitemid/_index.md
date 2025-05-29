---
title: AdvancedCompareOptions.IgnoreStoreItemId
linktitle: IgnoreStoreItemId
articleTitle: IgnoreStoreItemId
second_title: Aspose.Words per .NET
description: Scopri come la proprietà IgnoreStoreItemId di AdvancedCompareOptions migliora il confronto dei documenti ignorando le differenze degli ID StructuredDocumentTag per una maggiore precisione.
type: docs
weight: 30
url: /it/net/aspose.words.comparing/advancedcompareoptions/ignorestoreitemid/
---
## AdvancedCompareOptions.IgnoreStoreItemId property

Specifica se ignorare la differenza nell'ID elemento archivio StructuredDocumentTag.

```csharp
public bool IgnoreStoreItemId { get; set; }
```

## Osservazioni

Il valore predefinito è`falso` .

## Esempi

Mostra come confrontare SDT con lo stesso contenuto ma con ID articolo del negozio diverso.

```csharp
Document docA = new Document(MyDir + "Document with SDT 1.docx");
Document docB = new Document(MyDir + "Document with SDT 2.docx");

// Configura le opzioni per confrontare SDT con lo stesso contenuto ma con ID articolo del negozio diverso.
CompareOptions compareOptions = new CompareOptions();
compareOptions.AdvancedOptions.IgnoreStoreItemId = false;

docA.Compare(docB, "user", DateTime.Now, compareOptions);
Assert.AreEqual(8, docA.Revisions.Count);

compareOptions.AdvancedOptions.IgnoreStoreItemId = true;

docA.Revisions.RejectAll();
docA.Compare(docB, "user", DateTime.Now, compareOptions);
Assert.AreEqual(0, docA.Revisions.Count);
```

### Guarda anche

* class [AdvancedCompareOptions](../)
* spazio dei nomi [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* assemblea [Aspose.Words](../../../)
