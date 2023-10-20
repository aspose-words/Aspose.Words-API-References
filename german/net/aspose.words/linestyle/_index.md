---
title: LineStyle Enum
linktitle: LineStyle
articleTitle: LineStyle
second_title: Aspose.Words für .NET
description: Aspose.Words.LineStyle opsomming. Gibt den Linienstil von a anBorder  in C#.
type: docs
weight: 3450
url: /de/net/aspose.words/linestyle/
---
## LineStyle enumeration

Gibt den Linienstil von a an[`Border`](../border/) .

```csharp
public enum LineStyle
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` |  |
| Single | `1` |  |
| Thick | `2` |  |
| Double | `3` |  |
| Hairline | `5` |  |
| Dot | `6` |  |
| DashLargeGap | `7` |  |
| DotDash | `8` |  |
| DotDotDash | `9` |  |
| Triple | `10` |  |
| ThinThickSmallGap | `11` |  |
| ThickThinSmallGap | `12` |  |
| ThinThickThinSmallGap | `13` |  |
| ThinThickMediumGap | `14` |  |
| ThickThinMediumGap | `15` |  |
| ThinThickThinMediumGap | `16` |  |
| ThinThickLargeGap | `17` |  |
| ThickThinLargeGap | `18` |  |
| ThinThickThinLargeGap | `19` |  |
| Wave | `20` |  |
| DoubleWave | `21` |  |
| DashSmallGap | `22` |  |
| DashDotStroker | `23` |  |
| Emboss3D | `24` |  |
| Engrave3D | `25` |  |
| Outset | `26` |  |
| Inset | `27` |  |

## Beispiele

Zeigt, wie man eine von einem Rahmen umgebene Zeichenfolge in ein Dokument einfügt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
