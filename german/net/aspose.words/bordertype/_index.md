---
title: BorderType Enum
linktitle: BorderType
articleTitle: BorderType
second_title: Aspose.Words für .NET
description: Aspose.Words.BorderType opsomming. Gibt die Seiten eines Rahmens an in C#.
type: docs
weight: 100
url: /de/net/aspose.words/bordertype/
---
## BorderType enumeration

Gibt die Seiten eines Rahmens an.

Um mehr zu erfahren, besuchen Sie die[Programmieren mit Dokumenten](https://docs.aspose.com/words/net/programming-with-documents/) Dokumentationsartikel.

```csharp
public enum BorderType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `-1` | Standardwert. |
| Bottom | `0` | Gibt den unteren Rand eines Absatzes oder einer Tabellenzelle an. |
| Left | `1` | Gibt den linken Rand eines Absatzes oder einer Tabellenzelle an. |
| Right | `2` | Gibt den rechten Rand eines Absatzes oder einer Tabellenzelle an. |
| Top | `3` | Gibt den oberen Rand eines Absatzes oder einer Tabellenzelle an. |
| Horizontal | `4` | Gibt die horizontale Grenze zwischen Zellen in einer Tabelle oder zwischen konformen Absätzen an. |
| Vertical | `5` | Gibt den vertikalen Rand zwischen Zellen in einer Tabelle an. |
| DiagonalDown | `6` | Gibt den diagonalen Rand in einer Tabellenzelle an. |
| DiagonalUp | `7` | Gibt den diagonalen Rand in einer Tabellenzelle an. |

## Beispiele

Zeigt, wie ein Absatz mit einem oberen Rand eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders.Top;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;
// ThemeColor nur festlegen, wenn LineWidth oder LineStyle festgelegt ist.
topBorder.ThemeColor = ThemeColor.Accent1;
topBorder.TintAndShade = 0.25d;

builder.Writeln("Text with a top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
