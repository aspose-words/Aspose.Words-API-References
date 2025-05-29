---
title: CustomDocumentProperties.AddLinkToContent
linktitle: AddLinkToContent
articleTitle: AddLinkToContent
second_title: Aspose.Words för .NET
description: Upptäck metoden AddLinkToContent i CustomDocumentProperties för att enkelt skapa länkade anpassade dokumentegenskaper för förbättrad dokumenthantering.
type: docs
weight: 20
url: /sv/net/aspose.words.properties/customdocumentproperties/addlinktocontent/
---
## CustomDocumentProperties.AddLinkToContent method

Skapar en ny anpassad dokumentegenskap för länkat innehåll.

```csharp
public DocumentProperty AddLinkToContent(string name, string linkSource)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| name | String | Fastighetens namn. |
| linkSource | String | Egendomens källa. |

### Returvärde

Det nyskapade egenskapsobjektet eller`null` när den*linkSource* är ogiltig.

## Exempel

Visar hur man länkar en anpassad dokumentegenskap till ett bokmärke.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("MyBookmark");
builder.Write("Hello world!");
builder.EndBookmark("MyBookmark");

// Länka en ny anpassad egenskap till ett bokmärke. Värdet för denna egenskap
// kommer att vara innehållet i bokmärket som den refererar till i "LinkSource"-medlemmen.
CustomDocumentProperties customProperties = doc.CustomDocumentProperties;
DocumentProperty customProperty = customProperties.AddLinkToContent("Bookmark", "MyBookmark");

Assert.AreEqual(true, customProperty.IsLinkToContent);
Assert.AreEqual("MyBookmark", customProperty.LinkSource);
Assert.AreEqual("Hello world!", customProperty.Value);

doc.Save(ArtifactsDir + "DocumentProperties.LinkCustomDocumentPropertiesToBookmark.docx");
```

### Se även

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* namnutrymme [Aspose.Words.Properties](../../../aspose.words.properties/)
* hopsättning [Aspose.Words](../../../)
