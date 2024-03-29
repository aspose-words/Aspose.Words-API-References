---
title: OfficeMath.GetMathRenderer
linktitle: GetMathRenderer
articleTitle: GetMathRenderer
second_title: Aspose.Words för .NET
description: OfficeMath GetMathRenderer metod. Skapar och returnerar ett objekt som kan användas för att rendera denna ekvation till en bild i C#.
type: docs
weight: 70
url: /sv/net/aspose.words.math/officemath/getmathrenderer/
---
## OfficeMath.GetMathRenderer method

Skapar och returnerar ett objekt som kan användas för att rendera denna ekvation till en bild.

```csharp
public OfficeMathRenderer GetMathRenderer()
```

### Returvärde

Renderingsobjektet för denna ekvation.

## Anmärkningar

Denna metod åberopar bara[`OfficeMathRenderer`](../../../aspose.words.rendering/officemathrenderer/) constructor och passes detta objekt som en parameter.

## Exempel

Visar hur man renderar ett Office Math-objekt till en bildfil i det lokala filsystemet.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// Skapa ett "ImageSaveOptions"-objekt för att skicka till nodrenderarens "Save"-metod för att ändra
// hur det återger OfficeMath-noden till en bild.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// Ställ in egenskapen "Skala" till 5 för att återge objektet till fem gånger dess ursprungliga storlek.
saveOptions.Scale = 5;

math.GetMathRenderer().Save(ArtifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

### Se även

* class [OfficeMathRenderer](../../../aspose.words.rendering/officemathrenderer/)
* class [OfficeMath](../)
* namnutrymme [Aspose.Words.Math](../../../aspose.words.math/)
* hopsättning [Aspose.Words](../../../)
