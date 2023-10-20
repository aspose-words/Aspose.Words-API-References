---
title: Document.ViewOptions
linktitle: ViewOptions
articleTitle: ViewOptions
second_title: Aspose.Words für .NET
description: Document ViewOptions eigendom. Bietet Optionen zur Steuerung der Anzeige des Dokuments in Microsoft Word in C#.
type: docs
weight: 470
url: /de/net/aspose.words/document/viewoptions/
---
## Document.ViewOptions property

Bietet Optionen zur Steuerung der Anzeige des Dokuments in Microsoft Word.

```csharp
public ViewOptions ViewOptions { get; }
```

## Beispiele

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

* class [ViewOptions](../../../aspose.words.settings/viewoptions/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
