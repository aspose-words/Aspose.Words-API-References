---
title: PageSetup.CharactersPerLine
linktitle: CharactersPerLine
articleTitle: CharactersPerLine
second_title: Aspose.Words für .NET
description: PageSetup CharactersPerLine eigendom. Ruft die Anzahl der Zeichen pro Zeile im Dokumentraster ab oder legt diese fest in C#.
type: docs
weight: 100
url: /de/net/aspose.words/pagesetup/charactersperline/
---
## PageSetup.CharactersPerLine property

Ruft die Anzahl der Zeichen pro Zeile im Dokumentraster ab oder legt diese fest.

```csharp
public int CharactersPerLine { get; set; }
```

## Bemerkungen

Der Mindestwert der Eigenschaft ist 1. Der Höchstwert hängt von der Seitenbreite und der Schriftgröße des Normal -Stils ab. Der Mindestzeichenabstand beträgt 90 Prozent der Schriftgröße. Beispielsweise beträgt die maximale Anzahl von Zeichen pro Zeile einer Letter-Seite mit 1-Zoll-Rändern 43.

Standardmäßig hat die Eigenschaft einen Wert, bei dem der Zeichenabstand der Schriftgröße des Stils „Normal “ entspricht.

## Beispiele

Zeigt, wie man a für die Anzahl der Zeichen angibt, die jede Zeile enthalten darf.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Pitching aktivieren und dann verwenden, um die Anzahl der Zeichen pro Zeile in diesem Abschnitt festzulegen.
builder.PageSetup.LayoutMode = SectionLayoutMode.Grid;
builder.PageSetup.CharactersPerLine = 10;

// Die Anzahl der Zeichen hängt auch von der Größe der Schriftart ab.
doc.Styles["Normal"].Font.Size = 20;

Assert.AreEqual(8, doc.FirstSection.PageSetup.CharactersPerLine);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "PageSetup.CharactersPerLine.docx");
```

### Siehe auch

* class [PageSetup](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
