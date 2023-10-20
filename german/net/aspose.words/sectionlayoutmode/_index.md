---
title: SectionLayoutMode Enum
linktitle: SectionLayoutMode
articleTitle: SectionLayoutMode
second_title: Aspose.Words für .NET
description: Aspose.Words.SectionLayoutMode opsomming. Gibt den Layoutmodus für einen Abschnitt an der es ermöglicht das Verhalten des Dokumentrasters zu definieren in C#.
type: docs
weight: 5750
url: /de/net/aspose.words/sectionlayoutmode/
---
## SectionLayoutMode enumeration

Gibt den Layoutmodus für einen Abschnitt an, der es ermöglicht, das Verhalten des Dokumentrasters zu definieren.

```csharp
public enum SectionLayoutMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Default | `0` | Gibt an, dass kein Dokumentraster auf den Inhalt des entsprechenden Abschnitts im Dokument angewendet werden soll. |
| Grid | `1` | Gibt an, dass im entsprechenden Abschnitt sowohl der zusätzliche Zeilenabstand als auch der Zeichenabstand zu jeder Zeile und jedem darin enthaltenen Zeichen hinzugefügt werden sollen, um eine bestimmte Anzahl Zeilen pro Seite und Zeichen pro Zeile beizubehalten. Zeichen werden nicht automatisch an aktivierten Gitterlinien ausgerichtet tippen. |
| LineGrid | `2` | Gibt an, dass dem entsprechenden Abschnitt jeder Zeile innerhalb von it ein zusätzlicher Zeilenabstand hinzugefügt werden soll, um die angegebene Anzahl von Zeilen pro Seite beizubehalten. |
| SnapToChars | `3` | Gibt an, dass im entsprechenden Abschnitt sowohl der zusätzliche Zeilenabstand als auch der Zeichenabstand zu jeder Zeile und jedem darin enthaltenen Zeichen hinzugefügt werden sollen, um eine bestimmte Anzahl von Zeilen pro Seite und Zeichen pro Zeile beizubehalten. Zeichen werden bei der Eingabe automatisch an Gitterlinien ausgerichtet. |

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

Zeigt, wie Sie einen Grenzwert für die Anzahl der Zeilen festlegen, die jede Seite haben darf.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Pitching aktivieren und dann verwenden, um die Anzahl der Zeilen pro Seite in diesem Abschnitt festzulegen.
// Eine ausreichend große Schriftgröße verschiebt einige Zeilen nach unten auf die nächste Seite, um überlappende Zeichen zu vermeiden.
builder.PageSetup.LayoutMode = SectionLayoutMode.LineGrid;
builder.PageSetup.LinesPerPage = 15;

builder.ParagraphFormat.SnapToGrid = true;

for (int i = 0; i < 30; i++)
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

doc.Save(ArtifactsDir + "PageSetup.LinesPerPage.docx");
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
