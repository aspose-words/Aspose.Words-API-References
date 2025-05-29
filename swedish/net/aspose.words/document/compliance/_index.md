---
title: Document.Compliance
linktitle: Compliance
articleTitle: Compliance
second_title: Aspose.Words för .NET
description: Säkerställ att dina OOXML-dokument uppfyller kraven utan problem. Vårt verktyg analyserar innehåll för att verifiera OOXML-efterlevnad och förbättra dokumentintegriteten.
type: docs
weight: 70
url: /sv/net/aspose.words/document/compliance/
---
## Document.Compliance property

Hämtar OOXML-efterlevnadsversionen som bestäms från det laddade dokumentinnehållet. Gäller endast OOXML-dokument.

```csharp
public OoxmlCompliance Compliance { get; }
```

## Anmärkningar

Om du skapade ett nytt tomt dokument eller laddade ett dokument som inte är OOXML returnerar document Ecma376_2006 värde.

## Exempel

Visar hur man läser ett inläst dokuments Open Office XML-kompatibel version.

```csharp
// Versionen för efterlevnad varierar mellan dokument som skapats av olika versioner av Microsoft Word.
Document doc = new Document(MyDir + "Document.doc");
Assert.AreEqual(doc.Compliance, OoxmlCompliance.Ecma376_2006);

doc = new Document(MyDir + "Document.docx");
Assert.AreEqual(doc.Compliance, OoxmlCompliance.Iso29500_2008_Transitional);
```

### Se även

* enum [OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
