---
title: AdvancedCompareOptions Class
linktitle: AdvancedCompareOptions
articleTitle: AdvancedCompareOptions
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.AdvancedCompareOptions för kraftfull dokumentjämförelse. Anpassa inställningar för exakta resultat och förbättrad produktivitet.
type: docs
weight: 460
url: /sv/net/aspose.words.comparing/advancedcompareoptions/
---
## AdvancedCompareOptions class

Gör det möjligt att ställa in avancerade jämförelsealternativ.

```csharp
public class AdvancedCompareOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [AdvancedCompareOptions](advancedcompareoptions/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [IgnoreDmlUniqueId](../../aspose.words.comparing/advancedcompareoptions/ignoredmluniqueid/) { get; set; } | Anger om skillnaden i DrawingML:s unika ID ska ignoreras. |
| [IgnoreStoreItemId](../../aspose.words.comparing/advancedcompareoptions/ignorestoreitemid/) { get; set; } | Anger om skillnaden i StructuredDocumentTag-lagrets objekt-ID ska ignoreras. |

## Anmärkningar

Dessa alternativ saknar motsvarighet i Microsoft Word och kan bidra till att ge ett mer exakt jämförelseresultat.

## Exempel

Visar hur man jämför SDT med samma innehåll men olika artikel-ID i butiken.

```csharp
Document docA = new Document(MyDir + "Document with SDT 1.docx");
Document docB = new Document(MyDir + "Document with SDT 2.docx");

// Konfigurera alternativ för att jämföra SDT med samma innehåll men olika artikel-ID i butiken.
CompareOptions compareOptions = new CompareOptions();
compareOptions.AdvancedOptions.IgnoreStoreItemId = false;

docA.Compare(docB, "user", DateTime.Now, compareOptions);
Assert.AreEqual(8, docA.Revisions.Count);

compareOptions.AdvancedOptions.IgnoreStoreItemId = true;

docA.Revisions.RejectAll();
docA.Compare(docB, "user", DateTime.Now, compareOptions);
Assert.AreEqual(0, docA.Revisions.Count);
```

### Se även

* namnutrymme [Aspose.Words.Comparing](../../aspose.words.comparing/)
* hopsättning [Aspose.Words](../../)
