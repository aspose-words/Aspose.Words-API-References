---
title: ViewOptions.ViewType
second_title: Aspose.Words für .NET-API-Referenz
description: ViewOptions eigendom. Steuert den Ansichtsmodus in Microsoft Word.
type: docs
weight: 40
url: /de/net/aspose.words.settings/viewoptions/viewtype/
---
## ViewOptions.ViewType property

Steuert den Ansichtsmodus in Microsoft Word.

```csharp
public ViewType ViewType { get; set; }
```

### Bemerkungen

Obwohl Aspose.Words diese Option lesen und schreiben kann, ist ihre Verwendung anwendungsspezifisch. Beispielsweise berücksichtigt MS Word 2013 den Wert dieser Option nicht.

### Beispiele

Zeigt, wie Sie einen benutzerdefinierten Zoomfaktor festlegen, der ältere Versionen von Microsoft Word beim Laden auf ein Dokument anwenden.

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

### Siehe auch

* enum [ViewType](../../viewtype/)
* class [ViewOptions](../)
* namensraum [Aspose.Words.Settings](../../viewoptions/)
* Montage [Aspose.Words](../../../)


