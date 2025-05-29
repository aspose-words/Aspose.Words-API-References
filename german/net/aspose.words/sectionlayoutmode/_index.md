---
title: SectionLayoutMode Enum
linktitle: SectionLayoutMode
articleTitle: SectionLayoutMode
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.SectionLayoutMode, um Abschnittslayouts zu optimieren und das Dokumentrasterverhalten für eine verbesserte Formatierungskontrolle zu verbessern.
type: docs
weight: 6580
url: /de/net/aspose.words/sectionlayoutmode/
---
## SectionLayoutMode enumeration

Gibt den Layoutmodus für einen Abschnitt an und ermöglicht die Definition des Rasterverhaltens des Dokuments.

```csharp
public enum SectionLayoutMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Default | `0` | Gibt an, dass auf den Inhalt des entsprechenden Abschnitts im Dokument kein Dokumentraster angewendet werden soll. |
| Grid | `1` | Gibt an, dass im entsprechenden Abschnitt jeder Zeile und jedem Zeichen der zusätzliche Zeilenabstand und Zeichenabstand hinzugefügt werden soll, um eine bestimmte Anzahl von Zeilen pro Seite und Zeichen pro Zeile einzuhalten. Zeichen werden beim Tippen nicht automatisch an den Gitternetzlinien ausgerichtet. |
| LineGrid | `2` | Gibt an, dass im entsprechenden Abschnitt zu jeder Zeile ein zusätzlicher Zeilenabstand hinzugefügt werden soll, um die angegebene Zeilenanzahl pro Seite einzuhalten. |
| SnapToChars | `3` | Gibt an, dass im entsprechenden Abschnitt jeder Zeile und jedem Zeichen der zusätzliche Zeilen- und Zeichenabstand hinzugefügt werden soll, um eine bestimmte Anzahl von Zeilen pro Seite und Zeichen pro Zeile einzuhalten. Zeichen werden beim Tippen automatisch an den Gitternetzlinien ausgerichtet. |

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

Zeigt, wie Sie eine Begrenzung für die Zeilenanzahl festlegen, die jede Seite haben darf.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Pitching aktivieren und dann damit die Zeilenanzahl pro Seite in diesem Abschnitt festlegen.
// Eine ausreichend große Schriftgröße verschiebt einige Zeilen auf die nächste Seite, um überlappende Zeichen zu vermeiden.
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
