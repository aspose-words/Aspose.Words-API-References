---
title: AdvancedCompareOptions.IgnoreStoreItemId
linktitle: IgnoreStoreItemId
articleTitle: IgnoreStoreItemId
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die AdvancedCompareOptions-Eigenschaft „IgnoreStoreItemId“ den Dokumentvergleich verbessert, indem sie Unterschiede in der StructuredDocumentTag-ID ignoriert und so die Genauigkeit verbessert.
type: docs
weight: 30
url: /de/net/aspose.words.comparing/advancedcompareoptions/ignorestoreitemid/
---
## AdvancedCompareOptions.IgnoreStoreItemId property

Gibt an, ob Unterschiede in der StructuredDocumentTag-Store-Element-ID ignoriert werden sollen.

```csharp
public bool IgnoreStoreItemId { get; set; }
```

## Bemerkungen

Der Standardwert ist`FALSCH` .

## Beispiele

Zeigt, wie SDT mit gleichem Inhalt, aber unterschiedlicher Store-Artikel-ID verglichen wird.

```csharp
Document docA = new Document(MyDir + "Document with SDT 1.docx");
Document docB = new Document(MyDir + "Document with SDT 2.docx");

// Konfigurieren Sie Optionen zum Vergleichen von SDT mit gleichem Inhalt, aber unterschiedlicher Store-Artikel-ID.
CompareOptions compareOptions = new CompareOptions();
compareOptions.AdvancedOptions.IgnoreStoreItemId = false;

docA.Compare(docB, "user", DateTime.Now, compareOptions);
Assert.AreEqual(8, docA.Revisions.Count);

compareOptions.AdvancedOptions.IgnoreStoreItemId = true;

docA.Revisions.RejectAll();
docA.Compare(docB, "user", DateTime.Now, compareOptions);
Assert.AreEqual(0, docA.Revisions.Count);
```

### Siehe auch

* class [AdvancedCompareOptions](../)
* namensraum [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* Montage [Aspose.Words](../../../)
