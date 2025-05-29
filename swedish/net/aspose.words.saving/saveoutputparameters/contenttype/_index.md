---
title: SaveOutputParameters.ContentType
linktitle: ContentType
articleTitle: ContentType
second_title: Aspose.Words för .NET
description: Upptäck egenskapen SaveOutputParameters ContentType, som anger Internet Media Type för dina sparade dokument, vilket säkerställer korrekt filidentifiering.
type: docs
weight: 10
url: /sv/net/aspose.words.saving/saveoutputparameters/contenttype/
---
## SaveOutputParameters.ContentType property

Returnerar Content-Type-strängen (Internet Media Type) som identifierar typen av det sparade dokumentet.

```csharp
public string ContentType { get; }
```

## Exempel

Visar hur man kommer åt utdataparametrar för ett dokuments sparningsåtgärd.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Efter att vi sparat ett dokument kan vi komma åt Internet Media Type (MIME-typ) för det nyskapade utdatadokumentet.
SaveOutputParameters parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.doc");

Assert.AreEqual("application/msword", parameters.ContentType);

// Den här egenskapen ändras beroende på vilket format som sparas.
parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.pdf");

Assert.AreEqual("application/pdf", parameters.ContentType);
```

### Se även

* class [SaveOutputParameters](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
