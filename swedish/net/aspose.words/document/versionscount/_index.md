---
title: Document.VersionsCount
linktitle: VersionsCount
articleTitle: VersionsCount
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Document VersionsCount för att enkelt spåra antalet lagrade dokumentversioner i dina DOC-filer för bättre hantering och organisation.
type: docs
weight: 480
url: /sv/net/aspose.words/document/versionscount/
---
## Document.VersionsCount property

Hämtar antalet dokumentversioner som lagrades i DOC-dokumentet.

```csharp
public int VersionsCount { get; }
```

## Anmärkningar

Versioner i Microsoft Word nås via menyn Arkiv/Versioner. Microsoft Word stöder endast versioner för DOC-filer.

Den här egenskapen gör det möjligt att detektera om det fanns dokumentversioner lagrade i detta dokument innan det öppnades i Aspose.Words. Aspose.Words erbjuder inget annat stöd för dokumentversioner. Om du sparar detta dokument med Aspose.Words kommer dokumentet att sparas utan versioner.

## Exempel

Visar hur man arbetar med versionsräknarfunktionen i äldre Microsoft Word-dokument.

```csharp
Document doc = new Document(MyDir + "Versions.doc");

// Vi kan läsa den här egenskapen i ett dokument, men vi kan inte bevara den medan vi sparar.
Assert.AreEqual(4, doc.VersionsCount);

doc.Save(ArtifactsDir + "Document.VersionsCount.doc");
doc = new Document(ArtifactsDir + "Document.VersionsCount.doc");

Assert.AreEqual(0, doc.VersionsCount);
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
