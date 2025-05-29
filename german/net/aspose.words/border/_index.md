---
title: Border Class
linktitle: Border
articleTitle: Border
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Border, Ihre Lösung zum Anpassen von Objekträndern in Dokumenten. Optimieren Sie Ihre Projekte mit Präzision und Stil!
type: docs
weight: 270
url: /de/net/aspose.words/border/
---
## Border class

Stellt den Rand eines Objekts dar.

Um mehr zu erfahren, besuchen Sie die[Programmieren mit Dokumenten](https://docs.aspose.com/words/net/programming-with-documents/) Dokumentationsartikel.

```csharp
public class Border : InternableComplexAttr
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Color](../../aspose.words/border/color/) { get; set; } | Ruft die Rahmenfarbe ab oder legt sie fest. |
| [DistanceFromText](../../aspose.words/border/distancefromtext/) { get; set; } | Ruft den Abstand des Rahmens vom Text oder vom Seitenrand in Punkten ab oder legt ihn fest. |
| [IsVisible](../../aspose.words/border/isvisible/) { get; } | Rückgaben`WAHR` wenn die[`LineStyle`](./linestyle/) ist nichtNone . |
| [LineStyle](../../aspose.words/border/linestyle/) { get; set; } | Ruft den Rahmenstil ab oder legt ihn fest. |
| [LineWidth](../../aspose.words/border/linewidth/) { get; set; } | Ruft die Rahmenbreite in Punkten ab oder legt sie fest. |
| [Shadow](../../aspose.words/border/shadow/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob der Rahmen einen Schatten hat. |
| [ThemeColor](../../aspose.words/border/themecolor/) { get; set; } | Ruft die Designfarbe im angewendeten Farbschema ab oder legt sie fest, die diesem Border-Objekt zugeordnet ist. |
| [TintAndShade](../../aspose.words/border/tintandshade/) { get; set; } | Ruft einen Double-Wert ab oder legt ihn fest, der eine Farbe aufhellt oder abdunkelt. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [ClearFormatting](../../aspose.words/border/clearformatting/)() | Setzt die Rahmeneigenschaften auf die Standardwerte zurück. |
| [Equals](../../aspose.words/border/equals/#equals)(*Border*) | Bestimmt, ob der angegebene Rahmen dem aktuellen Rahmen im Wert entspricht. |
| override [Equals](../../aspose.words/border/equals/#equals_1)(*object*) | Bestimmt, ob das angegebene Objekt den gleichen Wert wie das aktuelle Objekt hat. |
| override [GetHashCode](../../aspose.words/border/gethashcode/)() | Dient als Hash-Funktion für diesen Typ. |

## Bemerkungen

Rahmen können auf verschiedene Dokumentelemente angewendet werden, einschließlich Absätzen, Textlauf innerhalb eines Absatzes oder einer Tabellenzelle.

## Beispiele

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

Zeigt, wie ein Absatz mit einem oberen Rand eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders.Top;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;
// ThemeColor nur festlegen, wenn LineWidth oder LineStyle festgelegt sind.
topBorder.ThemeColor = ThemeColor.Accent1;
topBorder.TintAndShade = 0.25d;

builder.Writeln("Text with a top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Siehe auch

* class [InternableComplexAttr](../internablecomplexattr/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
