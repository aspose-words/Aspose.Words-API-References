---
title: PageSetup.CharactersPerLine
linktitle: CharactersPerLine
articleTitle: CharactersPerLine
second_title: Aspose.Words für .NET
description: Steuern Sie Ihr Dokumentlayout mit der PageSetup-Eigenschaft „CharactersPerLine“. Passen Sie die Zeichen pro Zeile einfach an, um optimale Lesbarkeit und Design zu gewährleisten.
type: docs
weight: 100
url: /de/net/aspose.words/pagesetup/charactersperline/
---
## PageSetup.CharactersPerLine property

Ruft die Anzahl der Zeichen pro Zeile im Dokumentraster ab oder legt sie fest.

```csharp
public int CharactersPerLine { get; set; }
```

## Bemerkungen

Der Mindestwert der Eigenschaft ist 1. Der Maximalwert hängt von der Seitenbreite und der Schriftgröße des Stils „Normal “ ab. Der Mindestzeichenabstand beträgt 90 Prozent der Schriftgröße. Beispielsweise beträgt die maximale Anzahl von Zeichen pro Zeile einer Letter-Seite mit 2,5-cm-Rändern 43.

Standardmäßig hat die Eigenschaft einen Wert, bei dem der Zeichenabstand der Schriftgröße des Stils „Normal “ entspricht.

## Beispiele

Zeigt, wie Sie für die Anzahl der Zeichen angeben, die jede Zeile enthalten darf.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Pitching aktivieren und dann damit die Anzahl der Zeichen pro Zeile in diesem Abschnitt festlegen.
builder.PageSetup.LayoutMode = SectionLayoutMode.Grid;
builder.PageSetup.CharactersPerLine = 10;

// Die Anzahl der Zeichen hängt auch von der Schriftgröße ab.
doc.Styles["Normal"].Font.Size = 20;

Assert.AreEqual(8, doc.FirstSection.PageSetup.CharactersPerLine);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "PageSetup.CharactersPerLine.docx");
```

### Siehe auch

* class [PageSetup](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
