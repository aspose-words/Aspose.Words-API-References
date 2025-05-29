---
title: AdvancedCompareOptions Class
linktitle: AdvancedCompareOptions
articleTitle: AdvancedCompareOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.AdvancedCompareOptions für leistungsstarken Dokumentenvergleich. Passen Sie die Einstellungen für präzise Ergebnisse und gesteigerte Produktivität an.
type: docs
weight: 460
url: /de/net/aspose.words.comparing/advancedcompareoptions/
---
## AdvancedCompareOptions class

Ermöglicht das Festlegen erweiterter Vergleichsoptionen.

```csharp
public class AdvancedCompareOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [AdvancedCompareOptions](advancedcompareoptions/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [IgnoreDmlUniqueId](../../aspose.words.comparing/advancedcompareoptions/ignoredmluniqueid/) { get; set; } | Gibt an, ob Unterschiede in der eindeutigen DrawingML-ID ignoriert werden sollen. |
| [IgnoreStoreItemId](../../aspose.words.comparing/advancedcompareoptions/ignorestoreitemid/) { get; set; } | Gibt an, ob Unterschiede in der StructuredDocumentTag-Store-Element-ID ignoriert werden sollen. |

## Bemerkungen

Diese Optionen haben in Microsoft Word keine Entsprechung und können dazu beitragen, ein präziseres Vergleichsergebnis zu erzielen.

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

* namensraum [Aspose.Words.Comparing](../../aspose.words.comparing/)
* Montage [Aspose.Words](../../)
