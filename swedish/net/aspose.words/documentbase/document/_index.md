---
title: DocumentBase.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words för .NET
description: Utforska DocumentBase-egenskaper för att effektivt hantera dina dokument. Få sömlös åtkomst och förbättra ditt arbetsflöde idag!
type: docs
weight: 20
url: /sv/net/aspose.words/documentbase/document/
---
## DocumentBase.Document property

Hämtar denna instans.

```csharp
public override DocumentBase Document { get; }
```

## Exempel

Visar hur man skapar ett enkelt dokument.

```csharp
Document doc = new Document();

// Nya dokumentobjekt levereras som standard med den minimala uppsättningen noder
// krävs för att börja lägga till innehåll som text och former: ett avsnitt, en brödtext och ett stycke.
doc.AppendChild(new Section(doc))
    .AppendChild(new Body(doc))
    .AppendChild(new Paragraph(doc))
    .AppendChild(new Run(doc, "Hello world!"));
```

### Se även

* class [DocumentBase](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
