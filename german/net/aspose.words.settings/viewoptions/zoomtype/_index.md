---
title: ViewOptions.ZoomType
linktitle: ZoomType
articleTitle: ZoomType
second_title: Aspose.Words für .NET
description: Entdecken Sie die ZoomType-Eigenschaft von ViewOptions, um die Zoomstufen einfach an die Fenstergröße anzupassen und so das Benutzererlebnis und die Flexibilität der Schnittstelle zu verbessern.
type: docs
weight: 60
url: /de/net/aspose.words.settings/viewoptions/zoomtype/
---
## ViewOptions.ZoomType property

Ruft einen Zoomwert basierend auf der Fenstergröße ab oder legt ihn fest.

```csharp
public ZoomType ZoomType { get; set; }
```

## Beispiele

Zeigt, wie ein benutzerdefinierter Zoomfaktor festgelegt wird, den ältere Versionen von Microsoft Word beim Laden eines Dokuments anwenden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.ViewOptions.ViewType = ViewType.PageLayout;
doc.ViewOptions.ZoomPercent = 50;

Assert.AreEqual(ZoomType.Custom, doc.ViewOptions.ZoomType);
Assert.AreEqual(ZoomType.None, doc.ViewOptions.ZoomType);

doc.Save(ArtifactsDir + "ViewOptions.SetZoomPercentage.doc");
```

Zeigt, wie ein benutzerdefinierter Zoomtyp festgelegt wird, den ältere Versionen von Microsoft Word beim Laden auf ein Dokument anwenden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Setzen Sie die Eigenschaft „ZoomType“ auf „ZoomType.PageWidth“, um Microsoft Word zu erhalten
// um das Dokument automatisch auf die Seitenbreite zu zoomen.
// Setzen Sie die Eigenschaft „ZoomType“ auf „ZoomType.FullPage“, um Microsoft Word zu erhalten
// um das Dokument automatisch zu vergrößern und die gesamte erste Seite sichtbar zu machen.
// Setzen Sie die Eigenschaft „ZoomType“ auf „ZoomType.TextFit“, um Microsoft Word zu erhalten
// um das Dokument automatisch so zu vergrößern, dass es an die inneren Textränder der ersten Seite angepasst ist.
doc.ViewOptions.ZoomType = zoomType;

doc.Save(ArtifactsDir + "ViewOptions.SetZoomType.doc");
```

### Siehe auch

* enum [ZoomType](../../zoomtype/)
* class [ViewOptions](../)
* namensraum [Aspose.Words.Settings](../../../aspose.words.settings/)
* Montage [Aspose.Words](../../../)
