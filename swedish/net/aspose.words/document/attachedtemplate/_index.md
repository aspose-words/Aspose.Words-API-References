---
title: Document.AttachedTemplate
linktitle: AttachedTemplate
articleTitle: AttachedTemplate
second_title: Aspose.Words för .NET
description: Upptäck hur du effektivt hanterar din Document AttachedTemplate-egenskap. Ställ enkelt in eller hämta hela sökvägen till din dokumentmall för sömlös integration.
type: docs
weight: 20
url: /sv/net/aspose.words/document/attachedtemplate/
---
## Document.AttachedTemplate property

Hämtar eller anger den fullständiga sökvägen till mallen som är bifogad till dokumentet.

```csharp
public string AttachedTemplate { get; set; }
```

### Undantag

| undantag | skick |
| --- | --- |
| ArgumentNullException | Kastar om du försöker ställa in på en`null` värde. |

## Anmärkningar

Tom sträng betyder att dokumentet är kopplat till Normal-mallen.

## Exempel

Visar hur man ställer in en standardmall för dokument som inte har bifogade mallar.

```csharp
Document doc = new Document();

// Aktivera automatisk stiluppdatering, men bifoga inte ett malldokument.
doc.AutomaticallyUpdateStyles = true;

Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Eftersom det inte finns något malldokument fanns det ingenstans i dokumentet att spåra stiländringar.
// Använd ett SaveOptions-objekt för att automatiskt ställa in en mall
// om ett dokument som vi sparar inte har ett.
SaveOptions options = SaveOptions.CreateSaveOptions("Document.DefaultTemplate.docx");
options.DefaultTemplate = MyDir + "Business brochure.dotx";

doc.Save(ArtifactsDir + "Document.DefaultTemplate.docx", options);
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
