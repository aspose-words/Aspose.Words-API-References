---
title: PageSetup.PageHeight
linktitle: PageHeight
articleTitle: PageHeight
second_title: Aspose.Words für .NET
description: Entdecken Sie die PageSetup PageHeight-Eigenschaft, um die Höhe Ihres Dokuments in Punkten effizient zu verwalten und so Ihr Layout und Ihre Präsentation zu verbessern.
type: docs
weight: 310
url: /de/net/aspose.words/pagesetup/pageheight/
---
## PageSetup.PageHeight property

Gibt die Höhe der Seite in Punkten zurück oder legt sie fest.

```csharp
public double PageHeight { get; set; }
```

## Beispiele

Zeigt, wie Sie ein Bild einfügen und als Wasserzeichen verwenden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie das Bild in die Kopfzeile ein, damit es auf jeder Seite sichtbar ist.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");
shape.WrapType = WrapType.None;
shape.BehindText = true;

// Platzieren Sie das Bild in der Mitte der Seite.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermark.docx");
```

### Siehe auch

* class [PageSetup](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
