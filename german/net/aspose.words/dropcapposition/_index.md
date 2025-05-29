---
title: DropCapPosition Enum
linktitle: DropCapPosition
articleTitle: DropCapPosition
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.DropCapPosition, um Ihr Dokumentdesign zu verbessern, indem Sie einzigartige Initialen-Textpositionen für eine wirkungsvolle visuelle Wirkung definieren.
type: docs
weight: 1820
url: /de/net/aspose.words/dropcapposition/
---
## DropCapPosition enumeration

Gibt die Position für einen Initialentext an.

```csharp
public enum DropCapPosition
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Der Absatz hat keinen Initial. |
| Normal | `1` | Die Initiale wird innerhalb des Textrands des Ankerabsatzes positioniert. |
| Margin | `2` | Die Initiale wird außerhalb des Textrands des Ankerabsatzes positioniert. |

## Beispiele

Zeigt, wie man einen Initial erstellt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie einen Absatz mit einem großen Buchstaben ein, mit dem der Text im zweiten und dritten Absatz beginnt.
builder.Font.Size = 54;
builder.Writeln("L");

builder.Font.Size = 18;
builder.Writeln("orem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
builder.Writeln("Ut enim ad minim veniam, quis nostrud exercitation " +
                "ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Derzeit werden der zweite und dritte Absatz unter dem ersten angezeigt.
// Wir können den ersten Absatz über sein „ParagraphFormat“-Objekt in eine Initiale für die anderen Absätze umwandeln.
// Setzen Sie die Eigenschaft „DropCapPosition“ auf „DropCapPosition.Margin“, um den Initial zu platzieren
// außerhalb des linken Seitenrands, wenn unser Text von links nach rechts verläuft.
// Setzen Sie die Eigenschaft „DropCapPosition“ auf „DropCapPosition.Normal“, um den Initial innerhalb der Seitenränder zu platzieren
// und den restlichen Text darum herum zu wickeln.
// „DropCapPosition.None“ ist der Standardzustand für alle Absätze.
ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;
format.DropCapPosition = dropCapPosition;

doc.Save(ArtifactsDir + "ParagraphFormat.DropCap.docx");
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
