---
title: ShapeBase.Name
second_title: Aspose.Words für .NET-API-Referenz
description: ShapeBase eigendom. Ruft den optionalen Formnamen ab oder legt ihn fest.
type: docs
weight: 400
url: /de/net/aspose.words.drawing/shapebase/name/
---
## ShapeBase.Name property

Ruft den optionalen Formnamen ab oder legt ihn fest.

```csharp
public string Name { get; set; }
```

### Bemerkungen

Der Standardwert ist eine leere Zeichenfolge.

Kann nicht sein`Null`, kann aber eine leere Zeichenfolge sein.

### Beispiele

Zeigt, wie der alternative Text einer Form verwendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertShape(ShapeType.Cube, 150, 150);
shape.Name = "MyCube";

shape.AlternativeText = "Alt text for MyCube.";

// Wir können auf den alternativen Text einer Form zugreifen, indem wir mit der rechten Maustaste darauf klicken und dann über „AutoShape formatieren“ -> "Alt-Text".
doc.Save(ArtifactsDir + "Shape.AltText.docx");

// Speichern Sie das Dokument im HTML-Format und löschen Sie dann das verknüpfte Bild, das zu unserer Form gehört.
// Der Browser, der unseren HTML-Code liest, zeigt den Alternativtext anstelle des fehlenden Bildes an.
doc.Save(ArtifactsDir + "Shape.AltText.html");
File.Delete(ArtifactsDir + "Shape.AltText.001.png");
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../shapebase/)
* Montage [Aspose.Words](../../../)


