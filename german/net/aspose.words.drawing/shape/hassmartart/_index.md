---
title: Shape.HasSmartArt
second_title: Aspose.Words für .NET-API-Referenz
description: Shape eigendom. Gibt zurückWAHR wenn dasShape hat ein SmartArtObjekt.
type: docs
weight: 90
url: /de/net/aspose.words.drawing/shape/hassmartart/
---
## Shape.HasSmartArt property

Gibt zurück`WAHR` wenn das[`Shape`](../) hat ein SmartArt-Objekt.

```csharp
public bool HasSmartArt { get; }
```

### Beispiele

Zeigt, wie die Anzahl der Formen in einem Dokument mit SmartArt-Objekten gezählt wird.

```csharp
Document doc = new Document(MyDir + "SmartArt.docx");

int numberOfSmartArtShapes = doc.GetChildNodes(NodeType.Shape, true).Cast<Shape>().Count(shape => shape.HasSmartArt);

Assert.AreEqual(2, numberOfSmartArtShapes);
```

### Siehe auch

* class [Shape](../)
* namensraum [Aspose.Words.Drawing](../../shape/)
* Montage [Aspose.Words](../../../)


