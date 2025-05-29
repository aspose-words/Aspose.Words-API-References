---
title: SaveOutputParameters Class
linktitle: SaveOutputParameters
articleTitle: SaveOutputParameters
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Saving.SaveOutputParameters, som ger viktig information efter att dokumentet har sparats, vilket förbättrar din dokumenthanteringsupplevelse.
type: docs
weight: 6390
url: /sv/net/aspose.words.saving/saveoutputparameters/
---
## SaveOutputParameters class

Detta objekt returneras till anroparen efter att ett dokument har sparats och innehåller ytterligare information som har genererats eller beräknats under sparningsoperationen. Anroparen kan använda eller ignorera detta objekt.

För att lära dig mer, besök[Spara ett dokument](https://docs.aspose.com/words/net/save-a-document/) dokumentationsartikel.

```csharp
public class SaveOutputParameters
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [ContentType](../../aspose.words.saving/saveoutputparameters/contenttype/) { get; } | Returnerar Content-Type-strängen (Internet Media Type) som identifierar typen av det sparade dokumentet. |

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

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
