---
title: ShapeBase.HRef
linktitle: HRef
articleTitle: HRef
second_title: Aspose.Words für .NET
description: Entdecken Sie die ShapeBase HRef-Eigenschaft, um vollständige Hyperlink-Adressen für Ihre Formen einfach zu verwalten und so die Interaktivität und Funktionalität Ihres Designs zu verbessern.
type: docs
weight: 250
url: /de/net/aspose.words.drawing/shapebase/href/
---
## ShapeBase.HRef property

Ruft die vollständige Hyperlinkadresse für eine Form ab oder legt sie fest.

```csharp
public string HRef { get; set; }
```

## Bemerkungen

Der Standardwert ist eine leere Zeichenfolge.

Nachfolgend finden Sie Beispiele für gültige Werte für diese Eigenschaft:

Vollständige URI:`https://www.aspose.com/`.

Vollständiger Dateiname:`C:\\Eigene Dokumente\\SalesReport.doc`.

Relative URI:`../../../resource.txt`

Relativer Dateiname:`..\\Eigene Dokumente\\SalesReport.doc`.

Lesezeichen in einem anderen Dokument:`https://www.aspose.com/Products/Default.aspx#Suites`

Lesezeichen in diesem Dokument:`#BookmakName`.

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
