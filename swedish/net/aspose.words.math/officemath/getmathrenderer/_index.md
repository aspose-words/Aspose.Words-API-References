---
title: OfficeMath.GetMathRenderer
linktitle: GetMathRenderer
articleTitle: GetMathRenderer
second_title: Aspose.Words för .NET
description: Upptäck OfficeMaths GetMathRenderer-metod för att enkelt konvertera ekvationer till bilder och förbättra dina dokument med tydliga, professionella bilder.
type: docs
weight: 90
url: /sv/net/aspose.words.math/officemath/getmathrenderer/
---
## OfficeMath.GetMathRenderer method

Skapar och returnerar ett objekt som kan användas för att rendera denna ekvation till en bild.

```csharp
public OfficeMathRenderer GetMathRenderer()
```

### Returvärde

Renderer-objektet för denna ekvation.

## Anmärkningar

Den här metoden anropar bara[`OfficeMathRenderer`](../../../aspose.words.rendering/officemathrenderer/) konstruktorn och skickar detta objekt som en parameter.

## Exempel

Visar hur man renderar ett Office Math-objekt till en bildfil i det lokala filsystemet.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// Skapa ett "ImageSaveOptions"-objekt för att skicka till nodrenderarens "Save"-metod för att modifiera
// hur den renderar OfficeMath-noden till en bild.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// Sätt egenskapen "Scale" till 5 för att rendera objektet till fem gånger sin ursprungliga storlek.
saveOptions.Scale = 5;

math.GetMathRenderer().Save(ArtifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

### Se även

* class [OfficeMathRenderer](../../../aspose.words.rendering/officemathrenderer/)
* class [OfficeMath](../)
* namnutrymme [Aspose.Words.Math](../../../aspose.words.math/)
* hopsättning [Aspose.Words](../../../)
