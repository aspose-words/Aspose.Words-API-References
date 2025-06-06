---
title: ShapeBase.AlternativeText
linktitle: AlternativeText
articleTitle: AlternativeText
second_title: Aspose.Words für .NET
description: Entdecken Sie die ShapeBase AlternativeText-Eigenschaft, die die Zugänglichkeit verbessert, indem sie beschreibenden Text für Grafiken bereitstellt und so die Benutzererfahrung und SEO verbessert.
type: docs
weight: 20
url: /de/net/aspose.words.drawing/shapebase/alternativetext/
---
## ShapeBase.AlternativeText property

Definiert alternativen Text, der anstelle einer Grafik angezeigt werden soll.

```csharp
public string AlternativeText { get; set; }
```

## Bemerkungen

Der Standardwert ist eine leere Zeichenfolge.

## Beispiele

Zeigt, wie der alternative Text einer Form verwendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertShape(ShapeType.Cube, 150, 150);
shape.Name = "MyCube";

shape.AlternativeText = "Alt text for MyCube.";

// Auf den Alternativtext einer Form können wir zugreifen, indem wir mit der rechten Maustaste darauf klicken und dann über „AutoForm formatieren“ -> „Alternativtext“ gehen.
doc.Save(ArtifactsDir + "Shape.AltText.docx");

// Speichern Sie das Dokument im HTML-Format und löschen Sie dann das verknüpfte Bild, das zu unserer Form gehört.
// Der Browser, der unser HTML liest, zeigt den Alternativtext anstelle des fehlenden Bildes an.
doc.Save(ArtifactsDir + "Shape.AltText.html");
File.Delete(ArtifactsDir + "Shape.AltText.001.png");
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
