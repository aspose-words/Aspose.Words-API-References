---
title: DocumentBuilder.PageSetup
linktitle: PageSetup
articleTitle: PageSetup
second_title: Aspose.Words für .NET
description: Erkunden Sie die DocumentBuilder PageSetup-Eigenschaft, um auf die aktuellen Seiten- und Abschnittseinstellungen zuzugreifen und so die Formatierung und Layouteffizienz Ihres Dokuments zu verbessern.
type: docs
weight: 160
url: /de/net/aspose.words/documentbuilder/pagesetup/
---
## DocumentBuilder.PageSetup property

Gibt ein Objekt zurück, das die aktuellen Seiteneinstellungen und Abschnittseigenschaften darstellt.

```csharp
public PageSetup PageSetup { get; }
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

* class [PageSetup](../../pagesetup/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
