---
title: ViewOptions.ZoomPercent
second_title: Aspose.Words für .NET-API-Referenz
description: ViewOptions eigendom. Ruft den Prozentsatz zwischen 10 und 500 ab oder legt ihn fest mit dem Sie Ihr Dokument anzeigen möchten.
type: docs
weight: 50
url: /de/net/aspose.words.settings/viewoptions/zoompercent/
---
## ViewOptions.ZoomPercent property

Ruft den Prozentsatz (zwischen 10 und 500) ab oder legt ihn fest, mit dem Sie Ihr Dokument anzeigen möchten.

```csharp
public int ZoomPercent { get; set; }
```

### Bemerkungen

Wenn der Wert 0 ist, verwendet diese Eigenschaft stattdessen 100, andernfalls, wenn der Wert kleiner als 10 oder größer als 500 ist, löst diese Eigenschaft aus.

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

* class [ViewOptions](../)
* namensraum [Aspose.Words.Settings](../../viewoptions/)
* Montage [Aspose.Words](../../../)


