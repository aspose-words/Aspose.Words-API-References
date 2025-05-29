---
title: PageVerticalAlignment Enum
linktitle: PageVerticalAlignment
articleTitle: PageVerticalAlignment
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.PageVerticalAlignment für optimale Textausrichtung auf Seiten. Verbessern Sie das Layout Ihres Dokuments mit präziser vertikaler Ausrichtung!
type: docs
weight: 5100
url: /de/net/aspose.words/pageverticalalignment/
---
## PageVerticalAlignment enumeration

Gibt die vertikale Ausrichtung des Textes auf jeder Seite an.

```csharp
public enum PageVerticalAlignment
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Bottom | `3` | Der Text wird unten auf der Seite ausgerichtet. |
| Center | `1` | Der Text wird in der Mitte der Seite ausgerichtet. |
| Justify | `2` | Der Text wird so verteilt, dass er die Seite ausfüllt. |
| Top | `0` | Der Text wird oben auf der Seite ausgerichtet. |

## Beispiele

Zeigt, wie Sie Seiteneinrichtungseinstellungen auf Abschnitte in einem Dokument anwenden und zurücksetzen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ändern Sie die Seiteneinrichtungseigenschaften für den aktuellen Abschnitt des Builders und fügen Sie Text hinzu.
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.VerticalAlignment = PageVerticalAlignment.Center;
builder.Writeln("This is the first section, which landscape oriented with vertically centered text.");

// Wenn wir einen neuen Abschnitt mit einem Dokumentgenerator beginnen,
// Es werden die aktuellen Seiteneinrichtungseigenschaften des Builders übernommen.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(Orientation.Landscape, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Center, doc.Sections[1].PageSetup.VerticalAlignment);

// Wir können die Seiteneinrichtungseigenschaften mit der Methode „ClearFormatting“ auf ihre Standardwerte zurücksetzen.
builder.PageSetup.ClearFormatting();

Assert.AreEqual(Orientation.Portrait, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Top, doc.Sections[1].PageSetup.VerticalAlignment);

builder.Writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc.Save(ArtifactsDir + "PageSetup.ClearFormatting.docx");
```

### Siehe auch

* class [PageSetup](../pagesetup/)
* property [VerticalAlignment](../pagesetup/verticalalignment/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
