---
title: DocumentBuilder.PageSetup
second_title: Aspose.Words für .NET-API-Referenz
description: DocumentBuilder eigendom. Gibt ein Objekt zurück das die aktuellen Seiteneinstellungen und Abschnittseigenschaften darstellt.
type: docs
weight: 160
url: /de/net/aspose.words/documentbuilder/pagesetup/
---
## DocumentBuilder.PageSetup property

Gibt ein Objekt zurück, das die aktuellen Seiteneinstellungen und Abschnittseigenschaften darstellt.

```csharp
public PageSetup PageSetup { get; }
```

### Beispiele

Zeigt, wie Seiteneinrichtungseinstellungen auf Abschnitte in einem Dokument angewendet und wiederhergestellt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ändern Sie die Seiteneinrichtungseigenschaften für den aktuellen Abschnitt des Builders und fügen Sie Text hinzu.
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.VerticalAlignment = PageVerticalAlignment.Center;
builder.Writeln("This is the first section, which landscape oriented with vertically centered text.");

// Wenn wir einen neuen Abschnitt mit einem Document Builder beginnen,
// Es erbt die aktuellen Seiteneinrichtungseigenschaften des Builders.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(Orientation.Landscape, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Center, doc.Sections[1].PageSetup.VerticalAlignment);

// Mit der Methode „ClearFormatting“ können wir die Seiteneinrichtungseigenschaften auf ihre Standardwerte zurücksetzen.
builder.PageSetup.ClearFormatting();

Assert.AreEqual(Orientation.Portrait, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Top, doc.Sections[1].PageSetup.VerticalAlignment);

builder.Writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc.Save(ArtifactsDir + "PageSetup.ClearFormatting.docx");
```

### Siehe auch

* class [PageSetup](../../pagesetup/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../documentbuilder/)
* Montage [Aspose.Words](../../../)


