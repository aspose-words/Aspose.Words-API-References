---
title: ShapeBase.Target
second_title: Aspose.Words für .NET-API-Referenz
description: ShapeBase eigendom. Ruft den Zielrahmen für den FormHyperlink ab oder legt ihn fest.
type: docs
weight: 480
url: /de/net/aspose.words.drawing/shapebase/target/
---
## ShapeBase.Target property

Ruft den Zielrahmen für den Form-Hyperlink ab oder legt ihn fest.

```csharp
public string Target { get; set; }
```

### Bemerkungen

Der Standardwert ist eine leere Zeichenfolge.

### Beispiele

Zeigt, wie eine Form eingefügt wird, die ein Bild enthält und auch ein Hyperlink ist.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.HRef = "https://forum.aspose.com/";
shape.Target = "New Window";
shape.ScreenTip = "Aspose.Words Support Forums";

// Strg + Linksklick auf die Form in Microsoft Word öffnet ein neues Webbrowser-Fenster
// und führen Sie uns zum Hyperlink in der Eigenschaft "HRef".
doc.Save(ArtifactsDir + "Image.InsertImageWithHyperlink.docx");
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../shapebase/)
* Montage [Aspose.Words](../../../)


