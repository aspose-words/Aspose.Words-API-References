---
title: SaveOutputParameters.ContentType
second_title: Aspose.Words för .NET API Referens
description: SaveOutputParameters fast egendom. Returnerar strängen ContentType Internet Media Type som identifierar typen av det sparade dokumentet.
type: docs
weight: 10
url: /sv/net/aspose.words.saving/saveoutputparameters/contenttype/
---
## SaveOutputParameters.ContentType property

Returnerar strängen Content-Type (Internet Media Type) som identifierar typen av det sparade dokumentet.

```csharp
public string ContentType { get; }
```

### Exempel

Visar hur man kommer åt utdataparametrar för ett dokuments lagringsoperation.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// När vi har sparat ett dokument kan vi komma åt Internet Media Type (MIME-typ) för det nyskapade utdatadokumentet.
SaveOutputParameters parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.doc");

Assert.AreEqual("application/msword", parameters.ContentType);

// Den här egenskapen ändras beroende på sparaformatet.
parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.pdf");

Assert.AreEqual("application/pdf", parameters.ContentType);
```

### Se även

* class [SaveOutputParameters](../)
* namnutrymme [Aspose.Words.Saving](../../saveoutputparameters/)
* hopsättning [Aspose.Words](../../../)


