---
title: Document.Compliance
linktitle: Compliance
articleTitle: Compliance
second_title: Aspose.Words för .NET
description: Document Compliance fast egendom. Får OOXMLkompatibilitetsversionen fastställd från det inlästa dokumentinnehållet. Är meningsfullt endast för OOXMLdokument i C#.
type: docs
weight: 60
url: /sv/net/aspose.words/document/compliance/
---
## Document.Compliance property

Får OOXML-kompatibilitetsversionen fastställd från det inlästa dokumentinnehållet. Är meningsfullt endast för OOXML-dokument.

```csharp
public OoxmlCompliance Compliance { get; }
```

## Anmärkningar

Om du skapade ett nytt tomt dokument eller laddar icke OOXML returnerar document Ecma376_2006 värde.

## Exempel

Visar hur man läser ett laddat dokuments Open Office XML-kompatibilitetsversion.

```csharp
// Efterlevnadsversionen varierar mellan dokument som skapats av olika versioner av Microsoft Word.
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
