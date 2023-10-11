---
title: Shape.HasSmartArt
second_title: Aspose.Words för .NET API Referens
description: Shape fast egendom. ReturnerarSann om det härShape har ett SmartArtobjekt.
type: docs
weight: 90
url: /sv/net/aspose.words.drawing/shape/hassmartart/
---
## Shape.HasSmartArt property

Returnerar`Sann` om det här[`Shape`](../) har ett SmartArt-objekt.

```csharp
public bool HasSmartArt { get; }
```

### Exempel

Visar hur man räknar antalet former i ett dokument med SmartArt-objekt.

```csharp
Document doc = new Document(MyDir + "SmartArt.docx");

int numberOfSmartArtShapes = doc.GetChildNodes(NodeType.Shape, true).Cast<Shape>().Count(shape => shape.HasSmartArt);

Assert.AreEqual(2, numberOfSmartArtShapes);
```

### Se även

* class [Shape](../)
* namnutrymme [Aspose.Words.Drawing](../../shape/)
* hopsättning [Aspose.Words](../../../)


