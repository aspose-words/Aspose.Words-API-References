---
title: DropCapPosition Enum
linktitle: DropCapPosition
articleTitle: DropCapPosition
second_title: Aspose.Words für .NET
description: Aspose.Words.DropCapPosition opsomming. Gibt die Position für einen Initialtext an in C#.
type: docs
weight: 1410
url: /de/net/aspose.words/dropcapposition/
---
## DropCapPosition enumeration

Gibt die Position für einen Initialtext an.

```csharp
public enum DropCapPosition
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Der Absatz hat keine Initiale. |
| Normal | `1` | Die Initiale wird innerhalb des Textrandes des Ankerabsatzes positioniert. |
| Margin | `2` | Die Initiale wird außerhalb des Textrandes im Ankerabsatz positioniert. |

## Beispiele

Zeigt, wie man eine Initiale erstellt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Einen Absatz mit einem Großbuchstaben einfügen, mit dem der Text im zweiten und dritten Absatz beginnt.
builder.Font.Size = 54;
builder.Writeln("L");

builder.Font.Size = 18;
builder.Writeln("orem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
builder.Writeln("Ut enim ad minim veniam, quis nostrud exercitation " +
                "ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Derzeit werden der zweite und der dritte Absatz unter dem ersten angezeigt.
// Wir können den ersten Absatz über sein „ParagraphFormat“-Objekt als Initiale für die anderen Absätze konvertieren.
// Setzen Sie die Eigenschaft „DropCapPosition“ auf „DropCapPosition.Margin“, um die Initiale zu platzieren
// außerhalb des linken Seitenrandes, wenn unser Text von links nach rechts verläuft.
// Setzen Sie die Eigenschaft „DropCapPosition“ auf „DropCapPosition.Normal“, um die Initiale innerhalb der Seitenränder zu platzieren
// und um den Rest des Textes darum zu wickeln.
// „DropCapPosition.None“ ist der Standardstatus für alle Absätze.
ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;
format.DropCapPosition = dropCapPosition;

doc.Save(ArtifactsDir + "ParagraphFormat.DropCap.docx");
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
