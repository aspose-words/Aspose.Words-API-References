---
title: Document.ViewOptions
linktitle: ViewOptions
articleTitle: ViewOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „Document ViewOptions“, um Ihre Microsoft Word-Anzeigeeinstellungen für ein maßgeschneidertes Anzeigeerlebnis anzupassen.
type: docs
weight: 490
url: /de/net/aspose.words/document/viewoptions/
---
## Document.ViewOptions property

Bietet Optionen zur Steuerung der Anzeige des Dokuments in Microsoft Word.

```csharp
public ViewOptions ViewOptions { get; }
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

* class [ViewOptions](../../../aspose.words.settings/viewoptions/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
