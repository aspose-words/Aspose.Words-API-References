---
title: Document.VersionsCount
second_title: Aspose.Words för .NET API Referens
description: Document fast egendom. Hämtar antalet dokumentversioner som lagrades i DOCdokumentet.
type: docs
weight: 440
url: /sv/net/aspose.words/document/versionscount/
---
## Document.VersionsCount property

Hämtar antalet dokumentversioner som lagrades i DOC-dokumentet.

```csharp
public int VersionsCount { get; }
```

### Anmärkningar

Versioner i Microsoft Word nås via menyn Arkiv/Version. Microsoft Word stöder versioner endast för DOC-filer.

Denna egenskap gör det möjligt att upptäcka om det fanns dokumentversioner lagrade i detta document innan det öppnades i Aspose.Words. Aspose.Words ger inget annat stöd för dokumentversioner. Om du sparar detta dokument med Aspose.Words kommer dokumentet att sparas utan versioner.

### Exempel

Visar hur man arbetar med versionsräkningsfunktionen i äldre Microsoft Word-dokument.

```csharp
Document doc = new Document(MyDir + "Versions.doc");

// Vi kan läsa den här egenskapen för ett dokument, men vi kan inte bevara den medan vi sparar.
Assert.AreEqual(4, doc.VersionsCount);

doc.Save(ArtifactsDir + "Document.VersionsCount.doc");      
doc = new Document(ArtifactsDir + "Document.VersionsCount.doc");

Assert.AreEqual(0, doc.VersionsCount);
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../document/)
* hopsättning [Aspose.Words](../../../)


