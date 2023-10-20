---
title: ViewOptions.ZoomPercent
linktitle: ZoomPercent
articleTitle: ZoomPercent
second_title: Aspose.Words für .NET
description: ViewOptions ZoomPercent eigendom. Ruft den Prozentsatz zwischen 10 und 500 ab mit dem Sie Ihr Dokument anzeigen möchten oder legt diesen fest in C#.
type: docs
weight: 50
url: /de/net/aspose.words.settings/viewoptions/zoompercent/
---
## ViewOptions.ZoomPercent property

Ruft den Prozentsatz (zwischen 10 und 500) ab, mit dem Sie Ihr Dokument anzeigen möchten, oder legt diesen fest.

```csharp
public int ZoomPercent { get; set; }
```

## Bemerkungen

Wenn der Wert 0 ist, verwendet diese Eigenschaft stattdessen 100, andernfalls löst diese Eigenschaft aus, wenn der Wert kleiner als 10 oder größer als 500 ist.

Obwohl Aspose.Words diese Option lesen und schreiben kann, ist ihre Verwendung anwendungsspezifisch. Beispielsweise berücksichtigt MS Word 2013 den Wert dieser Option nicht.

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

### Siehe auch

* class [ViewOptions](../)
* namensraum [Aspose.Words.Settings](../../../aspose.words.settings/)
* Montage [Aspose.Words](../../../)
