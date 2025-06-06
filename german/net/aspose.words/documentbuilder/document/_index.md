---
title: DocumentBuilder.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words für .NET
description: Verwalten Sie Dokumenteigenschaften mühelos mit DocumentBuilder. Rufen Sie Ihr Dokumentobjekt einfach ab oder legen Sie es fest, um die Dokumentenverwaltung zu optimieren.
type: docs
weight: 90
url: /de/net/aspose.words/documentbuilder/document/
---
## DocumentBuilder.Document property

Ruft ab oder setzt die`Document` Objekt, an das dieses Objekt angehängt ist.

```csharp
public Document Document { get; set; }
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

* class [Document](../../document/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
