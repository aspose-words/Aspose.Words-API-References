---
title: Document.AutomaticallyUpdateStyles
linktitle: AutomaticallyUpdateStyles
articleTitle: AutomaticallyUpdateStyles
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen AutomaticallyUpdateStyles i MS Word säkerställer att dokumentets format synkroniseras med mallen varje gång du öppnar det, vilket förbättrar konsekvensen.
type: docs
weight: 30
url: /sv/net/aspose.words/document/automaticallyupdatestyles/
---
## Document.AutomaticallyUpdateStyles property

Hämtar eller anger en flagga som anger om formaten i dokumentet uppdateras för att matcha formaten i den bifogade mallen varje gång dokumentet öppnas i MS Word.

```csharp
public bool AutomaticallyUpdateStyles { get; set; }
```

## Exempel

Visar hur man bifogar en mall till ett dokument.

```csharp
Document doc = new Document();

// Microsoft Word-dokument levereras som standard med en bifogad mall som heter "Normal.dotm".
// Det finns ingen standardmall för tomma Aspose.Words-dokument.
Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Bifoga en mall och sätt sedan flaggan för att tillämpa stiländringar
// inom mallen till stilar i vårt dokument.
doc.AttachedTemplate = MyDir + "Business brochure.dotx";
doc.AutomaticallyUpdateStyles = true;

doc.Save(ArtifactsDir + "Document.AutomaticallyUpdateStyles.docx");
```

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
