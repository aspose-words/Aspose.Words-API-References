---
title: ShapeBase.HRef
linktitle: HRef
articleTitle: HRef
second_title: Aspose.Words för .NET
description: Upptäck ShapeBase HRef-egenskapen för att enkelt hantera fullständiga hyperlänkadresser för dina former, vilket förbättrar din designs interaktivitet och funktionalitet.
type: docs
weight: 250
url: /sv/net/aspose.words.drawing/shapebase/href/
---
## ShapeBase.HRef property

Hämtar eller anger den fullständiga hyperlänkadressen för en form.

```csharp
public string HRef { get; set; }
```

## Anmärkningar

Standardvärdet är en tom sträng.

Nedan följer exempel på giltiga värden för den här egenskapen:

Fullständig URI:`https://www.aspose.com/`.

Fullständigt filnamn:`C:\\Mina dokument\\Försäljningsrapport.doc`.

Relativ URI:`../../../resurs.txt`

Relativt filnamn:`..\\Mina dokument\\Försäljningsrapport.doc`.

Bokmärk i ett annat dokument:`https://www.aspose.com/Products/Default.aspx#Suites`

Bokmärk i detta dokument:`#BookmakName`.

## Exempel

Visar hur man infogar en form som innehåller en bild och som också är en hyperlänk.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.HRef = "https://forum.aspose.com/";
shape.Target = "New Window";
shape.ScreenTip = "Aspose.Words Support Forums";

// Ctrl + vänsterklicka på formen i Microsoft Word öppnar ett nytt webbläsarfönster
// och tar oss till hyperlänken i egenskapen "HRef".
doc.Save(ArtifactsDir + "Image.InsertImageWithHyperlink.docx");
```

### Se även

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
