---
title: Shape.HasSmartArt
linktitle: HasSmartArt
articleTitle: HasSmartArt
second_title: Aspose.Words für .NET
description: Shape HasSmartArt eigendom. Gibt zurückWAHR wenn dasShape hat ein SmartArtObjekt in C#.
type: docs
weight: 90
url: /de/net/aspose.words.drawing/shape/hassmartart/
---
## Shape.HasSmartArt property

Gibt zurück`WAHR` wenn das[`Shape`](../) hat ein SmartArt-Objekt.

```csharp
public bool HasSmartArt { get; }
```

## Beispiele

Zeigt, wie die Anzahl der Formen in einem Dokument mit SmartArt-Objekten gezählt wird.

```csharp
Document doc = new Document(MyDir + "SmartArt.docx");

int numberOfSmartArtShapes = doc.GetChildNodes(NodeType.Shape, true).Cast<Shape>().Count(shape => shape.HasSmartArt);

Assert.AreEqual(2, numberOfSmartArtShapes);
```

### Siehe auch

* class [Shape](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
