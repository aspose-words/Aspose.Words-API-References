---
title: ShapeBase.Name
second_title: Aspose.Words für .NET-API-Referenz
description: ShapeBase eigendom. Ruft den optionalen Formnamen ab oder legt ihn fest.
type: docs
weight: 380
url: /de/net/aspose.words.drawing/shapebase/name/
---
## ShapeBase.Name property

Ruft den optionalen Formnamen ab oder legt ihn fest.

```csharp
public string Name { get; set; }
```

### Bemerkungen

Standard ist eine leere Zeichenfolge.

Kann nicht null sein, kann aber eine leere Zeichenfolge sein.

### Beispiele

Zeigt, wie der alternative Text einer Form verwendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertShape(ShapeType.Cube, 150, 150);
shape.Name = "MyCube";

shape.AlternativeText = "Alt text for MyCube.";

// Wir können auf den alternativen Text einer Form zugreifen, indem wir mit der rechten Maustaste darauf klicken und dann über "AutoForm formatieren" -> "Alt-Text".
doc.Save(ArtifactsDir + "Shape.AltText.docx");

// Speichern Sie das Dokument in HTML und löschen Sie dann das verknüpfte Bild, das zu unserer Form gehört.
// Der Browser, der unser HTML liest, zeigt den Alt-Text anstelle des fehlenden Bildes an.
doc.Save(ArtifactsDir + "Shape.AltText.html");
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../shapebase/)
* Montage [Aspose.Words](../../../)


