---
title: AdvancedCompareOptions Class
linktitle: AdvancedCompareOptions
articleTitle: AdvancedCompareOptions
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.AdvancedCompareOptions per un potente confronto di documenti. Personalizza le impostazioni per risultati precisi e una maggiore produttività.
type: docs
weight: 460
url: /it/net/aspose.words.comparing/advancedcompareoptions/
---
## AdvancedCompareOptions class

Consente di impostare opzioni di confronto avanzate.

```csharp
public class AdvancedCompareOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [AdvancedCompareOptions](advancedcompareoptions/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [IgnoreDmlUniqueId](../../aspose.words.comparing/advancedcompareoptions/ignoredmluniqueid/) { get; set; } | Specifica se ignorare la differenza nell'ID univoco di DrawingML. |
| [IgnoreStoreItemId](../../aspose.words.comparing/advancedcompareoptions/ignorestoreitemid/) { get; set; } | Specifica se ignorare la differenza nell'ID elemento archivio StructuredDocumentTag. |

## Osservazioni

Queste opzioni non hanno equivalenza in Microsoft Word e potrebbero aiutare a produrre risultati di confronto più precisi.

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

* spazio dei nomi [Aspose.Words.Comparing](../../aspose.words.comparing/)
* assemblea [Aspose.Words](../../)
