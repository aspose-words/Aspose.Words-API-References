---
title: BuiltInDocumentProperties.SharedDocument
linktitle: SharedDocument
articleTitle: SharedDocument
second_title: Aspose.Words för .NET
description: Upptäck funktionen BuiltInDocumentProperties SharedDocument som avslöjar om ditt dokument är delat, vilket förbättrar samarbete och tillgänglighet.
type: docs
weight: 280
url: /sv/net/aspose.words.properties/builtindocumentproperties/shareddocument/
---
## BuiltInDocumentProperties.SharedDocument property

Anger om dokumentet är ett delat dokument.

```csharp
public bool SharedDocument { get; }
```

## Anmärkningar

Aspose.Words uppdaterar inte den här egenskapen.

## Exempel

Visar hur man får utökade egenskaper.

```csharp
Document doc = new Document(MyDir + "Extended properties.docx");
Assert.IsTrue(doc.BuiltInDocumentProperties.ScaleCrop);
Assert.IsTrue(doc.BuiltInDocumentProperties.SharedDocument);
Assert.IsTrue(doc.BuiltInDocumentProperties.HyperlinksChanged);
```

### Se även

* class [BuiltInDocumentProperties](../)
* namnutrymme [Aspose.Words.Properties](../../../aspose.words.properties/)
* hopsättning [Aspose.Words](../../../)
