---
title: Shape.HasSmartArt
linktitle: HasSmartArt
articleTitle: HasSmartArt
second_title: Aspose.Words för .NET
description: Ta reda på om din form har ett SmartArt-objekt med egenskapen HasSmartArt. Lås upp kreativa designmöjligheter för dina projekt!
type: docs
weight: 100
url: /sv/net/aspose.words.drawing/shape/hassmartart/
---
## Shape.HasSmartArt property

Returer`sann` om detta[`Shape`](../) har ett SmartArt-objekt.

```csharp
public bool HasSmartArt { get; }
```

## Exempel

Visar hur man räknar antalet former i ett dokument med SmartArt-objekt.

```csharp
Document doc = new Document(MyDir + "SmartArt.docx");

int numberOfSmartArtShapes = doc.GetChildNodes(NodeType.Shape, true).Cast<Shape>().Count(shape => shape.HasSmartArt);

Assert.AreEqual(2, numberOfSmartArtShapes);
```

### Se även

* class [Shape](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
