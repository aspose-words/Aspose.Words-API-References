---
title: Class Border
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Border klas. Repräsentiert einen Rand eines Objekts.
type: docs
weight: 70
url: /de/net/aspose.words/border/
---
## Border class

Repräsentiert einen Rand eines Objekts.

```csharp
public class Border : InternableComplexAttr
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Color](../../aspose.words/border/color/) { get; set; } | Ruft die Rahmenfarbe ab oder legt sie fest. |
| [DistanceFromText](../../aspose.words/border/distancefromtext/) { get; set; } | Ermittelt oder setzt den Abstand des Rahmens vom Text oder vom Seitenrand in Punkt. |
| [IsVisible](../../aspose.words/border/isvisible/) { get; } | Gibt „true“ zurück, wenn der LineStyle nicht LineStyle.None ist. |
| [LineStyle](../../aspose.words/border/linestyle/) { get; set; } | Ruft den Rahmenstil ab oder legt ihn fest. |
| [LineWidth](../../aspose.words/border/linewidth/) { get; set; } | Liest oder setzt die Rahmenbreite in Punkt. |
| [Shadow](../../aspose.words/border/shadow/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob der Rahmen einen Schatten hat. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [ClearFormatting](../../aspose.words/border/clearformatting/)() | Setzt Rahmeneigenschaften auf Standardwerte zurück. |
| [Equals](../../aspose.words/border/equals/#equals)(Border) | Bestimmt, ob der angegebene Rand im Wert gleich dem aktuellen Rand ist. |
| override [Equals](../../aspose.words/border/equals/#equals_1)(object) | Bestimmt, ob das angegebene Objekt im Wert dem aktuellen Objekt entspricht. |
| override [GetHashCode](../../aspose.words/border/gethashcode/)() | dient als Hash-Funktion für diesen Typ. |

### Bemerkungen

Rahmen können auf verschiedene Dokumentelemente angewendet werden, einschließlich Absatz, Textverlauf innerhalb eines Absatzes oder einer Tabellenzelle.

### Beispiele

Zeigt, wie eine von einem Rahmen umgebene Zeichenfolge in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

Zeigt, wie Sie einen Absatz mit einem oberen Rand einfügen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders[BorderType.Top];
topBorder.Color = Color.Red;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;

builder.Writeln("Text with a red top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Siehe auch

* class [InternableComplexAttr](../internablecomplexattr/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)


