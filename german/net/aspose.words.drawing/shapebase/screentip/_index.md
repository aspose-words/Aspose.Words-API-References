---
title: ShapeBase.ScreenTip
linktitle: ScreenTip
articleTitle: ScreenTip
second_title: Aspose.Words für .NET
description: Entdecken Sie die ShapeBase-ScreenTip-Eigenschaft und verbessern Sie das Benutzererlebnis, indem Sie den Tooltip-Text anpassen, der angezeigt wird, wenn Sie mit der Maus über die Formen fahren.
type: docs
weight: 510
url: /de/net/aspose.words.drawing/shapebase/screentip/
---
## ShapeBase.ScreenTip property

Definiert den Text, der angezeigt wird, wenn der Mauszeiger über die Form bewegt wird.

```csharp
public string ScreenTip { get; set; }
```

## Bemerkungen

Der Standardwert ist eine leere Zeichenfolge.

## Beispiele

Zeigt, wie eine Form eingefügt wird, die ein Bild enthält und gleichzeitig ein Hyperlink ist.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.HRef = "https://forum.aspose.com/";
shape.Target = "New Window";
shape.ScreenTip = "Aspose.Words Support Forums";

// Strg + Linksklick auf die Form in Microsoft Word öffnet ein neues Webbrowserfenster
// und bringen uns zum Hyperlink in der Eigenschaft „HRef“.
doc.Save(ArtifactsDir + "Image.InsertImageWithHyperlink.docx");
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
