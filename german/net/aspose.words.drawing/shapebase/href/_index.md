---
title: ShapeBase.HRef
second_title: Aspose.Words für .NET-API-Referenz
description: ShapeBase eigendom. Ruft die vollständige HyperlinkAdresse für eine Form ab oder legt diese fest.
type: docs
weight: 230
url: /de/net/aspose.words.drawing/shapebase/href/
---
## ShapeBase.HRef property

Ruft die vollständige Hyperlink-Adresse für eine Form ab oder legt diese fest.

```csharp
public string HRef { get; set; }
```

### Bemerkungen

Der Standardwert ist eine leere Zeichenfolge.

Nachfolgend finden Sie Beispiele für gültige Werte für diese Eigenschaft:

Vollständiger URI:`https://www.aspose.com/`.

Vollständiger Dateiname:`C:\\Eigene Dateien\\SalesReport.doc`.

Relativer URI:`../../../resource.txt`

Relativer Dateiname:`..\\Eigene Dateien\\SalesReport.doc`.

Lesezeichen in einem anderen Dokument:`https://www.aspose.com/Products/Default.aspx#Suites`

Lesezeichen in diesem Dokument:`#BookmakName`.

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


