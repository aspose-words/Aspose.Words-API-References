---
title: SaveOutputParameters
second_title: Aspose.Words för .NET API Referens
description: Detta objekt returneras till den som ringer efter att ett dokument har sparats och innehåller ytterligare information som har genererats eller beräknats under sparoperationen. Den som ringer kan använda eller ignorera detta objekt.
type: docs
weight: 5310
url: /sv/net/aspose.words.saving/saveoutputparameters/
---
## SaveOutputParameters class

Detta objekt returneras till den som ringer efter att ett dokument har sparats och innehåller ytterligare information som har genererats eller beräknats under sparoperationen. Den som ringer kan använda eller ignorera detta objekt.

```csharp
public class SaveOutputParameters
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [ContentType](../../aspose.words.saving/saveoutputparameters/contenttype) { get; } | Returnerar strängen Content-Type (Internet Media Type) som identifierar typen av det sparade dokumentet. |

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

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->