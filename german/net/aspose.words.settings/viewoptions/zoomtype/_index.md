---
title: ViewOptions.ZoomType
second_title: Aspose.Words für .NET-API-Referenz
description: ViewOptions eigendom. Ruft einen Zoomwert basierend auf der Größe des Fensters ab oder legt diesen fest.
type: docs
weight: 60
url: /de/net/aspose.words.settings/viewoptions/zoomtype/
---
## ViewOptions.ZoomType property

Ruft einen Zoomwert basierend auf der Größe des Fensters ab oder legt diesen fest.

```csharp
public ZoomType ZoomType { get; set; }
```

### Beispiele

Zeigt, wie man einen benutzerdefinierten Zoomfaktor festlegt, den ältere Versionen von Microsoft Word beim Laden auf ein Dokument anwenden.

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

Zeigt, wie Sie einen benutzerdefinierten Zoomtyp festlegen, den ältere Versionen von Microsoft Word beim Laden auf ein Dokument anwenden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Setzen Sie die Eigenschaft „ZoomType“ auf „ZoomType.PageWidth“, um Microsoft Word abzurufen
// um das Dokument automatisch an die Breite der Seite anzupassen.
// Setzen Sie die Eigenschaft „ZoomType“ auf „ZoomType.FullPage“, um Microsoft Word abzurufen
// um das Dokument automatisch zu zoomen, um die gesamte erste Seite sichtbar zu machen.
// Setzen Sie die Eigenschaft „ZoomType“ auf „ZoomType.TextFit“, um Microsoft Word abzurufen
// um das Dokument automatisch so zu vergrößern, dass es in die inneren Textränder der ersten Seite passt.
doc.ViewOptions.ZoomType = zoomType;

doc.Save(ArtifactsDir + "ViewOptions.SetZoomType.doc");
```

### Siehe auch

* enum [ZoomType](../../zoomtype/)
* class [ViewOptions](../)
* namensraum [Aspose.Words.Settings](../../viewoptions/)
* Montage [Aspose.Words](../../../)


