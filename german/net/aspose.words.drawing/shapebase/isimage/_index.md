---
title: ShapeBase.IsImage
linktitle: IsImage
articleTitle: IsImage
second_title: Aspose.Words für .NET
description: Ermitteln Sie mit der IsImage-Eigenschaft von ShapeBase, ob eine Form ein Bild ist. Identifizieren Sie Bildformen ganz einfach für mehr Designflexibilität und Funktionalität.
type: docs
weight: 300
url: /de/net/aspose.words.drawing/shapebase/isimage/
---
## ShapeBase.IsImage property

Rückgaben`WAHR` wenn diese Form eine Bildform ist.

```csharp
public bool IsImage { get; }
```

## Beispiele

Zeigt, wie ein HTML-Dokument mit Bildern aus einem Stream unter Verwendung einer Basis-URI geöffnet wird.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Übergeben Sie die URI des Basisordners beim Laden
    // damit alle Bilder mit relativen URIs im HTML-Dokument gefunden werden können.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.BaseUri = ImageDir;

    Document doc = new Document(stream, loadOptions);

    // Überprüfen Sie, ob die erste Form des Dokuments ein gültiges Bild enthält.
    Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    Assert.IsTrue(shape.IsImage);
    Assert.IsNotNull(shape.ImageData.ImageBytes);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Width), 0.01);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Height), 0.01);
}
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
