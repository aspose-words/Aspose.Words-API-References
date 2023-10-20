---
title: Document.AttachedTemplate
linktitle: AttachedTemplate
articleTitle: AttachedTemplate
second_title: Aspose.Words för .NET
description: Document AttachedTemplate fast egendom. Hämtar eller ställer in hela sökvägen för mallen som är bifogad till dokumentet i C#.
type: docs
weight: 20
url: /sv/net/aspose.words/document/attachedtemplate/
---
## Document.AttachedTemplate property

Hämtar eller ställer in hela sökvägen för mallen som är bifogad till dokumentet.

```csharp
public string AttachedTemplate { get; set; }
```

### Undantag

| undantag | skick |
| --- | --- |
| ArgumentNullException | Kastar om du försöker ställa in till a`null` värde. |

## Anmärkningar

Tom sträng betyder att dokumentet är bifogat till mallen Normal.

## Exempel

Visar hur man ställer in en standardmall för dokument som inte har bifogade mallar.

```csharp
Document doc = new Document();

// Aktivera automatisk stiluppdatering, men bifoga inte ett malldokument.
doc.AutomaticallyUpdateStyles = true;

Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Eftersom det inte finns något malldokument hade dokumentet ingenstans att spåra stiländringar.
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
