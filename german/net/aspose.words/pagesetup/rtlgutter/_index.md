---
title: PageSetup.RtlGutter
linktitle: RtlGutter
articleTitle: RtlGutter
second_title: Aspose.Words für .NET
description: PageSetup RtlGutter eigendom. Ruft ab oder legt fest ob Microsoft Word für den Abschnitt Zwischenstege basierend auf einer RechtsnachLinksSprache oder einer LinksnachrechtsSprache verwendet in C#.
type: docs
weight: 380
url: /de/net/aspose.words/pagesetup/rtlgutter/
---
## PageSetup.RtlGutter property

Ruft ab oder legt fest, ob Microsoft Word für den Abschnitt Zwischenstege basierend auf einer Rechts-nach-Links-Sprache oder einer Links-nach-rechts-Sprache verwendet.

```csharp
public bool RtlGutter { get; set; }
```

## Beispiele

Zeigt, wie Bundstegränder festgelegt werden.

```csharp
Document doc = new Document();

// Text einfügen, der sich über mehrere Seiten erstreckt.
DocumentBuilder builder = new DocumentBuilder(doc);
for (int i = 0; i < 6; i++)
{
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                  "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
    builder.InsertBreak(BreakType.PageBreak);
}

// Ein Bundsteg fügt Leerzeichen entweder am linken oder rechten Seitenrand hinzu,
// wodurch das Falten in der Mitte eines Buchs ausgeglichen wird, das das Seitenlayout beeinträchtigt.
PageSetup pageSetup = doc.Sections[0].PageSetup;

// Bestimmen Sie, wie viel Platz unsere Seiten für Text innerhalb der Ränder haben, und fügen Sie dann einen Betrag hinzu, um einen Rand aufzufüllen.
Assert.AreEqual(470.30d, pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin, 0.01d);

pageSetup.Gutter = 100.0d;

// Setzen Sie die Eigenschaft „RtlGutter“ auf „true“, um den Bundsteg an einer geeigneteren Position für Text von rechts nach links zu platzieren.
pageSetup.RtlGutter = true;

// Setzen Sie die Eigenschaft „MultiplePages“ auf „MultiplePagesType.MirrorMargins“, um zu wechseln
// die linke/rechte Seitenposition der Ränder jeder Seite.
pageSetup.MultiplePages = MultiplePagesType.MirrorMargins;

doc.Save(ArtifactsDir + "PageSetup.Gutter.docx");
```

### Siehe auch

* class [PageSetup](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
