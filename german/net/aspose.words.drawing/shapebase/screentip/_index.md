---
title: ShapeBase.ScreenTip
second_title: Aspose.Words für .NET-API-Referenz
description: ShapeBase eigendom. Definiert den Text der angezeigt wird wenn der Mauszeiger über die Form bewegt.
type: docs
weight: 480
url: /de/net/aspose.words.drawing/shapebase/screentip/
---
## ShapeBase.ScreenTip property

Definiert den Text, der angezeigt wird, wenn der Mauszeiger über die Form bewegt.

```csharp
public string ScreenTip { get; set; }
```

### Bemerkungen

Der Standardwert ist eine leere Zeichenfolge.

### Beispiele

Zeigt, wie eine Form eingefügt wird, die ein Bild enthält und gleichzeitig einen Hyperlink darstellt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.HRef = "https://forum.aspose.com/";
shape.Target = "New Window";
shape.ScreenTip = "Aspose.Words Support Forums";

// Strg + Linksklick auf die Form in Microsoft Word öffnet ein neues Webbrowser-Fenster
// und führen Sie uns zum Hyperlink in der Eigenschaft „HRef“.
doc.Save(ArtifactsDir + "Image.InsertImageWithHyperlink.docx");
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../shapebase/)
* Montage [Aspose.Words](../../../)


