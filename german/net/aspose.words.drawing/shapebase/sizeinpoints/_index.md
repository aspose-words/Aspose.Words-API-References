---
title: ShapeBase.SizeInPoints
linktitle: SizeInPoints
articleTitle: SizeInPoints
second_title: Aspose.Words für .NET
description: Entdecken Sie die ShapeBase SizeInPoints-Eigenschaft, um Formabmessungen in Punkten einfach abzurufen und zu verwalten und so eine präzise Designkontrolle zu gewährleisten.
type: docs
weight: 540
url: /de/net/aspose.words.drawing/shapebase/sizeinpoints/
---
## ShapeBase.SizeInPoints property

Ruft die Größe der Form in Punkten ab.

```csharp
public SizeF SizeInPoints { get; }
```

## Beispiele

Zeigt, wie die Größe und Auszeichnungssprache einer Form überprüft wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Dml, shape.MarkupLanguage);
Assert.AreEqual(new SizeF(300, 300), shape.SizeInPoints);
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
