---
title: ShapeBase.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words für .NET
description: Entdecken Sie die ShapeBase-Name-Eigenschaft, um optionale Formnamen einfach zu verwalten und so Ihre Designflexibilität und Projektorganisation zu verbessern.
type: docs
weight: 420
url: /de/net/aspose.words.drawing/shapebase/name/
---
## ShapeBase.Name property

Ruft den optionalen Formnamen ab oder legt ihn fest.

```csharp
public string Name { get; set; }
```

## Bemerkungen

Der Standardwert ist eine leere Zeichenfolge.

Kann nicht sein`null`, kann aber eine leere Zeichenfolge sein.

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
