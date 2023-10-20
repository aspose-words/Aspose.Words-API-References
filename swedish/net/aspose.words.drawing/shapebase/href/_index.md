---
title: ShapeBase.HRef
linktitle: HRef
articleTitle: HRef
second_title: Aspose.Words för .NET
description: ShapeBase HRef fast egendom. Hämtar eller ställer in den fullständiga hyperlänkadressen för en form i C#.
type: docs
weight: 230
url: /sv/net/aspose.words.drawing/shapebase/href/
---
## ShapeBase.HRef property

Hämtar eller ställer in den fullständiga hyperlänkadressen för en form.

```csharp
public string HRef { get; set; }
```

## Anmärkningar

Standardvärdet är en tom sträng.

Nedan finns exempel på giltiga värden för den här egenskapen:

Fullständig URI:`https://www.aspose.com/`.

Fullständigt filnamn:`C:\\Mina dokument\\Säljrapport.doc`.

Relativ URI:`../../../resource.txt`

Relativt filnamn:`..\\Mina dokument\\Försäljningsrapport.doc`.

Bokmärk i ett annat dokument:`https://www.aspose.com/Products/Default.aspx#Suites`

Bokmärk i detta dokument:`#BookmakName`.

## Exempel

Visar hur man infogar en form som innehåller en bild och är också en hyperlänk.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.HRef = "https://forum.aspose.com/";
shape.Target = "New Window";
shape.ScreenTip = "Aspose.Words Support Forums";

// Ctrl + vänsterklicka på formen i Microsoft Word öppnar ett nytt webbläsarfönster
// och ta oss till hyperlänken i egenskapen "HRef".
doc.Save(ArtifactsDir + "Image.InsertImageWithHyperlink.docx");
```

### Se även

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
