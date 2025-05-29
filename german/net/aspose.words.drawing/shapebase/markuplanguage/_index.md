---
title: ShapeBase.MarkupLanguage
linktitle: MarkupLanguage
articleTitle: MarkupLanguage
second_title: Aspose.Words für .NET
description: Entdecken Sie die ShapeBase MarkupLanguage-Eigenschaft für verbessertes Grafikobjektmanagement. Profitieren Sie noch heute von nahtloser Integration und verbesserter Designeffizienz!
type: docs
weight: 410
url: /de/net/aspose.words.drawing/shapebase/markuplanguage/
---
## ShapeBase.MarkupLanguage property

Ruft die für dieses Grafikobjekt verwendete MarkupLanguage ab.

```csharp
public ShapeMarkupLanguage MarkupLanguage { get; }
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

* enum [ShapeMarkupLanguage](../../shapemarkuplanguage/)
* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
