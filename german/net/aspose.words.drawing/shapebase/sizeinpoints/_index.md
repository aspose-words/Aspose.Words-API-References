---
title: ShapeBase.SizeInPoints
second_title: Aspose.Words für .NET-API-Referenz
description: ShapeBase eigendom. Ermittelt die Größe der Form in Punkten.
type: docs
weight: 510
url: /de/net/aspose.words.drawing/shapebase/sizeinpoints/
---
## ShapeBase.SizeInPoints property

Ermittelt die Größe der Form in Punkten.

```csharp
public SizeF SizeInPoints { get; }
```

### Beispiele

Zeigt, wie Sie die Größe und Markup-Sprache einer Form überprüfen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Dml, shape.MarkupLanguage);
Assert.AreEqual(new SizeF(300, 300), shape.SizeInPoints);
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../shapebase/)
* Montage [Aspose.Words](../../../)


