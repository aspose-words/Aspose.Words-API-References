---
title: Border Class
linktitle: Border
articleTitle: Border
second_title: Aspose.Words für .NET
description: Aspose.Words.Border klas. Stellt einen Rand eines Objekts dar in C#.
type: docs
weight: 80
url: /de/net/aspose.words/border/
---
## Border class

Stellt einen Rand eines Objekts dar.

Um mehr zu erfahren, besuchen Sie die[Programmieren mit Dokumenten](https://docs.aspose.com/words/net/programming-with-documents/) Dokumentationsartikel.

```csharp
public class Border : InternableComplexAttr
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Color](../../aspose.words/border/color/) { get; set; } | Ruft die Rahmenfarbe ab oder legt sie fest. |
| [DistanceFromText](../../aspose.words/border/distancefromtext/) { get; set; } | Ermittelt oder legt den Abstand des Rahmens vom Text oder vom Seitenrand in Punkten fest. |
| [IsVisible](../../aspose.words/border/isvisible/) { get; } | Gibt zurück`WAHR` wenn die[`LineStyle`](./linestyle/) ist nichtNone . |
| [LineStyle](../../aspose.words/border/linestyle/) { get; set; } | Ruft den Rahmenstil ab oder legt ihn fest. |
| [LineWidth](../../aspose.words/border/linewidth/) { get; set; } | Ruft die Rahmenbreite in Punkten ab oder legt sie fest. |
| [Shadow](../../aspose.words/border/shadow/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der angibt, ob der Rahmen einen Schatten hat. |
| [ThemeColor](../../aspose.words/border/themecolor/) { get; set; } | Ruft die Designfarbe im angewendeten Farbschema ab, das diesem Border-Objekt zugeordnet ist, oder legt diese fest. |
| [TintAndShade](../../aspose.words/border/tintandshade/) { get; set; } | Ruft einen Double-Wert ab oder legt ihn fest, der eine Farbe heller oder dunkler macht. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [ClearFormatting](../../aspose.words/border/clearformatting/)() | Setzt die Randeigenschaften auf die Standardwerte zurück. |
| [Equals](../../aspose.words/border/equals/#equals)(*Border*) | Bestimmt, ob der angegebene Rahmen den gleichen Wert wie der aktuelle Rahmen hat. |
| override [Equals](../../aspose.words/border/equals/#equals_1)(*object*) | Bestimmt, ob das angegebene Objekt den gleichen Wert wie das aktuelle Objekt hat. |
| override [GetHashCode](../../aspose.words/border/gethashcode/)() | Dient als Hash-Funktion für diesen Typ. |

## Bemerkungen

Rahmen können auf verschiedene Dokumentelemente angewendet werden, einschließlich Absätze, Textläufe innerhalb eines Absatzes oder einer Tabellenzelle.

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

* class [InternableComplexAttr](../internablecomplexattr/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
