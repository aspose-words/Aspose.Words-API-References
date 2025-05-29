---
title: PageSetup.VerticalAlignment
linktitle: VerticalAlignment
articleTitle: VerticalAlignment
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die PageSetup VerticalAlignment-Eigenschaft das Dokumentlayout verbessert, indem sie die Textausrichtung für eine bessere Lesbarkeit und Darstellung anpasst.
type: docs
weight: 450
url: /de/net/aspose.words/pagesetup/verticalalignment/
---
## PageSetup.VerticalAlignment property

Gibt die vertikale Ausrichtung des Textes auf jeder Seite in einem Dokument oder Abschnitt zurück oder legt sie fest.

```csharp
public PageVerticalAlignment VerticalAlignment { get; set; }
```

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

* enum [PageVerticalAlignment](../../pageverticalalignment/)
* class [PageSetup](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
