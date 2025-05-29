---
title: ViewOptions.ZoomPercent
linktitle: ZoomPercent
articleTitle: ZoomPercent
second_title: Aspose.Words für .NET
description: Passen Sie die ZoomPercent-Eigenschaft von ViewOptions an, um die Zoomstufe Ihres Dokuments zwischen 10 und 500 % einzustellen. Verbessern Sie die Lesbarkeit und optimieren Sie Ihr Seherlebnis!
type: docs
weight: 50
url: /de/net/aspose.words.settings/viewoptions/zoompercent/
---
## ViewOptions.ZoomPercent property

Ruft den Prozentsatz ab, mit dem Sie Ihr Dokument anzeigen möchten, oder legt diesen fest.

```csharp
public int ZoomPercent { get; set; }
```

## Bemerkungen

Obwohl Aspose.Words diese Option lesen und schreiben kann, ist ihre Verwendung anwendungsspezifisch. Beispielsweise respektiert MS Word 2013 den Wert dieser Option nicht.

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

### Siehe auch

* class [ViewOptions](../)
* namensraum [Aspose.Words.Settings](../../../aspose.words.settings/)
* Montage [Aspose.Words](../../../)
