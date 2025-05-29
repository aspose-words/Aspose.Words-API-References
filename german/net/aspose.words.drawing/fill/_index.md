---
title: Fill Class
linktitle: Fill
articleTitle: Fill
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Drawing.Fill für erweiterte Füllformatierungsoptionen, mit denen Sie das Design und die visuelle Attraktivität Ihres Dokuments mühelos verbessern können.
type: docs
weight: 1270
url: /de/net/aspose.words.drawing/fill/
---
## Fill class

Stellt die Füllformatierung für ein Objekt dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit grafischen Elementen](https://docs.aspose.com/words/net/working-with-graphic-elements/) Dokumentationsartikel.

```csharp
public class Fill
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BackColor](../../aspose.words.drawing/fill/backcolor/) { get; set; } | Ruft ein Color-Objekt ab oder legt es fest, das die Hintergrundfarbe für die Füllung darstellt. |
| [BackThemeColor](../../aspose.words.drawing/fill/backthemecolor/) { get; set; } | Ruft ein ThemeColor-Objekt ab oder legt es fest, das die Hintergrundfarbe für die Füllung darstellt. |
| [BackTintAndShade](../../aspose.words.drawing/fill/backtintandshade/) { get; set; } | Ruft einen Double-Wert ab oder legt ihn fest, der die Hintergrundfarbe aufhellt oder abdunkelt. |
| [BaseForeColor](../../aspose.words.drawing/fill/baseforecolor/) { get; } | Ruft ein Farbobjekt ab, das die Basisvordergrundfarbe für die Füllung ohne Modifikatoren darstellt. |
| [Color](../../aspose.words.drawing/fill/color/) { get; set; } | Ruft ein Color-Objekt ab oder legt es fest, das die Vordergrundfarbe für die Füllung darstellt. |
| [FillType](../../aspose.words.drawing/fill/filltype/) { get; } | Ruft einen Fülltyp ab. |
| [ForeColor](../../aspose.words.drawing/fill/forecolor/) { get; set; } | Ruft ein Color-Objekt ab oder legt es fest, das die Vordergrundfarbe für die Füllung darstellt. |
| [ForeThemeColor](../../aspose.words.drawing/fill/forethemecolor/) { get; set; } | Ruft ein ThemeColor-Objekt ab oder legt es fest, das die Vordergrundfarbe für die Füllung darstellt. |
| [ForeTintAndShade](../../aspose.words.drawing/fill/foretintandshade/) { get; set; } | Ruft einen Double-Wert ab oder legt ihn fest, der die Vordergrundfarbe aufhellt oder abdunkelt. |
| [GradientAngle](../../aspose.words.drawing/fill/gradientangle/) { get; set; } | Ruft den Winkel der Verlaufsfüllung ab oder legt ihn fest. |
| [GradientStops](../../aspose.words.drawing/fill/gradientstops/) { get; } | Ruft eine Sammlung von[`GradientStop`](../gradientstop/) Objekte für die Füllung. |
| [GradientStyle](../../aspose.words.drawing/fill/gradientstyle/) { get; } | Ruft den Farbverlaufsstil ab[`GradientStyle`](../gradientstyle/) für die Füllung. |
| [GradientVariant](../../aspose.words.drawing/fill/gradientvariant/) { get; } | Ruft die Gradientenvariante ab[`GradientVariant`](../gradientvariant/) für die Füllung. |
| [ImageBytes](../../aspose.words.drawing/fill/imagebytes/) { get; } | Ruft die Rohbytes der Fülltextur oder des Musters ab. |
| [Opacity](../../aspose.words.drawing/fill/opacity/) { get; set; } | Ruft den Grad der Deckkraft der angegebenen Füllung als Wert zwischen 0,0 (klar) und 1,0 (undurchsichtig) ab oder legt ihn fest. |
| [Pattern](../../aspose.words.drawing/fill/pattern/) { get; } | Erhält eine[`PatternType`](../patterntype/) für die Füllung. |
| [PresetTexture](../../aspose.words.drawing/fill/presettexture/) { get; } | Erhält eine[`PresetTexture`](../presettexture/) für die Füllung. |
| [RotateWithObject](../../aspose.words.drawing/fill/rotatewithobject/) { get; set; } | Ruft ab oder legt fest, ob die Füllung mit dem angegebenen Objekt rotiert. |
| [TextureAlignment](../../aspose.words.drawing/fill/texturealignment/) { get; set; } | Ruft die Ausrichtung für die Kacheltexturfüllung ab oder legt sie fest. |
| [Transparency](../../aspose.words.drawing/fill/transparency/) { get; set; } | Ruft den Transparenzgrad der angegebenen Füllung als Wert zwischen 0,0 (undurchsichtig) und 1,0 (transparent) ab oder legt ihn fest. |
| [Visible](../../aspose.words.drawing/fill/visible/) { get; set; } | Ruft einen Wert ab oder setzt ihn`WAHR` wenn die auf diese Instanz angewendete Formatierung sichtbar ist. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [OneColorGradient](../../aspose.words.drawing/fill/onecolorgradient/#onecolorgradient)(*[GradientStyle](../gradientstyle/), [GradientVariant](../gradientvariant/), double*) | Legt die angegebene Füllung auf einen einfarbigen Farbverlauf fest. |
| [OneColorGradient](../../aspose.words.drawing/fill/onecolorgradient/#onecolorgradient_1)(*Color, [GradientStyle](../gradientstyle/), [GradientVariant](../gradientvariant/), double*) | Legt die angegebene Füllung auf einen einfarbigen Farbverlauf mit der angegebenen Farbe fest. |
| [Patterned](../../aspose.words.drawing/fill/patterned/#patterned)(*[PatternType](../patterntype/)*) | Legt die angegebene Füllung auf ein Muster fest. |
| [Patterned](../../aspose.words.drawing/fill/patterned/#patterned_1)(*[PatternType](../patterntype/), Color, Color*) | Legt die angegebene Füllung auf ein Muster fest. |
| [PresetTextured](../../aspose.words.drawing/fill/presettextured/)(*[PresetTexture](../presettexture/)*) | Legt die Füllung auf eine voreingestellte Textur fest. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage)(*byte[]*) | Ändert den Fülltyp in Einzelbild. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage_1)(*Stream*) | Ändert den Fülltyp in Einzelbild. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage_2)(*string*) | Ändert den Fülltyp in Einzelbild. |
| [Solid](../../aspose.words.drawing/fill/solid/#solid)() | Legt die Füllung auf eine einheitliche Farbe fest. |
| [Solid](../../aspose.words.drawing/fill/solid/#solid_1)(*Color*) | Legt die Füllung auf eine angegebene einheitliche Farbe fest. |
| [TwoColorGradient](../../aspose.words.drawing/fill/twocolorgradient/#twocolorgradient)(*[GradientStyle](../gradientstyle/), [GradientVariant](../gradientvariant/)*) | Legt die angegebene Füllung auf einen zweifarbigen Farbverlauf fest. |
| [TwoColorGradient](../../aspose.words.drawing/fill/twocolorgradient/#twocolorgradient_1)(*Color, Color, [GradientStyle](../gradientstyle/), [GradientVariant](../gradientvariant/)*) | Legt die angegebene Füllung auf einen zweifarbigen Farbverlauf fest. |

## Bemerkungen

Verwenden Sie die[`Fill`](../shapebase/fill/) oder[`Fill`](../../aspose.words/font/fill/) Eigenschaft, um auf Fülleigenschaften eines Objekts zuzugreifen. Sie erstellen keine Instanzen der`Fill` Klasse direkt.

## Beispiele

Zeigt, wie eine Form mit einer Volltonfarbe gefüllt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Schreiben Sie einen Text und bedecken Sie ihn dann mit einer schwebenden Form.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// Verwenden Sie die Eigenschaft „StrokeColor“, um die Farbe des Umrisses der Form festzulegen.
shape.StrokeColor = Color.CadetBlue;

// Verwenden Sie die Eigenschaft „FillColor“, um die Farbe des Innenbereichs der Form festzulegen.
shape.FillColor = Color.LightBlue;

// Die Eigenschaft „Deckkraft“ bestimmt, wie transparent die Farbe auf einer Skala von 0 bis 1 ist.
// wobei 1 völlig undurchsichtig und 0 unsichtbar ist.
// Die Formfüllung ist standardmäßig vollständig undurchsichtig, sodass wir den Text, über dem sich diese Form befindet, nicht sehen können.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// Stellen Sie die Deckkraft der Formfüllfarbe auf einen niedrigeren Wert ein, damit wir den Text darunter sehen können.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
