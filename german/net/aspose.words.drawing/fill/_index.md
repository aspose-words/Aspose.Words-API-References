---
title: Class Fill
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Drawing.Fill klas. Stellt die Füllformatierung für ein Objekt dar.
type: docs
weight: 820
url: /de/net/aspose.words.drawing/fill/
---
## Fill class

Stellt die Füllformatierung für ein Objekt dar.

```csharp
public class Fill
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BackColor](../../aspose.words.drawing/fill/backcolor/) { get; set; } | Ruft ein Color-Objekt ab oder legt es fest, das die Hintergrundfarbe für die Füllung darstellt. |
| [FillType](../../aspose.words.drawing/fill/filltype/) { get; } | Ruft einen Fülltyp ab. |
| [ForeColor](../../aspose.words.drawing/fill/forecolor/) { get; set; } | Ruft ein Color-Objekt ab oder legt es fest, das die Vordergrundfarbe für die Füllung darstellt. |
| [GradientAngle](../../aspose.words.drawing/fill/gradientangle/) { get; set; } | Ruft den Winkel der Verlaufsfüllung ab oder legt ihn fest. |
| [GradientStops](../../aspose.words.drawing/fill/gradientstops/) { get; } | Ruft eine Sammlung von ab[`GradientStop`](../gradientstop/) Objekte für die Füllung. |
| [GradientStyle](../../aspose.words.drawing/fill/gradientstyle/) { get; } | Ruft den Verlaufsstil ab[`GradientStyle`](../gradientstyle/) für die Füllung. |
| [GradientVariant](../../aspose.words.drawing/fill/gradientvariant/) { get; } | Ruft die Verlaufsvariante ab[`GradientVariant`](../gradientvariant/) für die Füllung. |
| [ImageBytes](../../aspose.words.drawing/fill/imagebytes/) { get; } | Ruft die Rohbytes der Fülltextur oder des Füllmusters ab. |
| [Opacity](../../aspose.words.drawing/fill/opacity/) { get; set; } | Ruft den Deckkraftgrad der angegebenen Füllung als Wert zwischen 0,0 (durchsichtig) und 1,0 (undurchsichtig) ab oder legt ihn fest. |
| [Pattern](../../aspose.words.drawing/fill/pattern/) { get; } | erhält a[`PatternType`](../patterntype/) für die Füllung. |
| [PresetTexture](../../aspose.words.drawing/fill/presettexture/) { get; } | erhält a[`PresetTexture`](../presettexture/) für die Füllung. |
| [RotateWithObject](../../aspose.words.drawing/fill/rotatewithobject/) { get; set; } | Ruft ab oder legt fest, ob sich die Füllung mit dem angegebenen Objekt dreht. |
| [TextureAlignment](../../aspose.words.drawing/fill/texturealignment/) { get; set; } | Ruft die Ausrichtung für die Kacheltexturfüllung ab oder legt sie fest. |
| [Transparency](../../aspose.words.drawing/fill/transparency/) { get; set; } | Ruft den Transparenzgrad der angegebenen Füllung als Wert zwischen 0,0 (deckend) und 1,0 (klar) ab oder legt ihn fest. |
| [Visible](../../aspose.words.drawing/fill/visible/) { get; set; } | Holt oder legt den Wert fest`Stimmt` wenn die auf diese Instanz angewendete Formatierung sichtbar ist. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [OneColorGradient](../../aspose.words.drawing/fill/onecolorgradient/#onecolorgradient)(GradientStyle, GradientVariant, double) | Legt die angegebene Füllung auf einen einfarbigen Farbverlauf fest. |
| [OneColorGradient](../../aspose.words.drawing/fill/onecolorgradient/#onecolorgradient_1)(Color, GradientStyle, GradientVariant, double) | Setzt die angegebene Füllung auf einen einfarbigen Farbverlauf mit der angegebenen Farbe. |
| [Patterned](../../aspose.words.drawing/fill/patterned/#patterned)(PatternType) | Legt die angegebene Füllung auf ein Muster fest. |
| [Patterned](../../aspose.words.drawing/fill/patterned/#patterned_1)(PatternType, Color, Color) | Legt die angegebene Füllung auf ein Muster fest. |
| [PresetTextured](../../aspose.words.drawing/fill/presettextured/)(PresetTexture) | Legt die Füllung auf eine voreingestellte Textur fest. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage)(byte[]) | Ändert den Fülltyp in Einzelbild. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage_1)(Stream) | Ändert den Fülltyp in Einzelbild. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage_2)(string) | Ändert den Fülltyp in Einzelbild. |
| [Solid](../../aspose.words.drawing/fill/solid/#solid)() | Setzt die Füllung auf eine einheitliche Farbe. |
| [Solid](../../aspose.words.drawing/fill/solid/#solid_1)(Color) | Legt die Füllung auf eine angegebene einheitliche Farbe fest. |
| [TwoColorGradient](../../aspose.words.drawing/fill/twocolorgradient/#twocolorgradient)(GradientStyle, GradientVariant) | Legt die angegebene Füllung auf einen zweifarbigen Farbverlauf fest. |
| [TwoColorGradient](../../aspose.words.drawing/fill/twocolorgradient/#twocolorgradient_1)(Color, Color, GradientStyle, GradientVariant) | Legt die angegebene Füllung auf einen zweifarbigen Farbverlauf fest. |

### Bemerkungen

Verwenden Sie die[`Fill`](../shapebase/fill/) oder[`Fill`](../../aspose.words/font/fill/) -Eigenschaft, um auf Fülleigenschaften eines Objekts zuzugreifen. Sie erstellen keine Instanzen von`Fill` Klasse direkt.

### Beispiele

Zeigt, wie eine Form mit einer Volltonfarbe gefüllt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Schreiben Sie etwas Text und bedecken Sie ihn dann mit einer schwebenden Form.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// Verwenden Sie die Eigenschaft "StrokeColor", um die Farbe des Umrisses der Form festzulegen.
shape.StrokeColor = Color.CadetBlue;

// Verwenden Sie die Eigenschaft "FillColor", um die Farbe des Innenbereichs der Form festzulegen.
shape.FillColor = Color.LightBlue;

// Die Eigenschaft "Deckkraft" bestimmt, wie transparent die Farbe auf einer Skala von 0-1 ist,
// wobei 1 vollständig undurchsichtig und 0 unsichtbar ist.
// Die Formfüllung ist standardmäßig vollständig undurchsichtig, sodass wir den Text, auf dem sich diese Form befindet, nicht sehen können.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// Setzen Sie die Deckkraft der Füllfarbe der Form auf einen niedrigeren Wert, damit wir den Text darunter sehen können.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)


