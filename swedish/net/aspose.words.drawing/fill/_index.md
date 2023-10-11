---
title: Class Fill
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Drawing.Fill klass. Representerar fyllningsformatering för ett objekt.
type: docs
weight: 950
url: /sv/net/aspose.words.drawing/fill/
---
## Fill class

Representerar fyllningsformatering för ett objekt.

För att lära dig mer, besök[Arbeta med grafiska element](https://docs.aspose.com/words/net/working-with-graphic-elements/) dokumentationsartikel.

```csharp
public class Fill
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [BackColor](../../aspose.words.drawing/fill/backcolor/) { get; set; } | Hämtar eller ställer in ett färgobjekt som representerar bakgrundsfärgen för fyllningen. |
| [BackThemeColor](../../aspose.words.drawing/fill/backthemecolor/) { get; set; } | Hämtar eller ställer in ett ThemeColor-objekt som representerar bakgrundsfärgen för fyllningen. |
| [BackTintAndShade](../../aspose.words.drawing/fill/backtintandshade/) { get; set; } | Hämtar eller ställer in ett dubbelt värde som gör bakgrundsfärgen ljusare eller mörkare. |
| [BaseForeColor](../../aspose.words.drawing/fill/baseforecolor/) { get; } |  |
| [Color](../../aspose.words.drawing/fill/color/) { get; set; } | Hämtar eller ställer in ett färgobjekt som representerar förgrundsfärgen för fyllningen. |
| [FillType](../../aspose.words.drawing/fill/filltype/) { get; } | Får en fyllningstyp. |
| [ForeColor](../../aspose.words.drawing/fill/forecolor/) { get; set; } | Hämtar eller ställer in ett färgobjekt som representerar förgrundsfärgen för fyllningen. |
| [ForeThemeColor](../../aspose.words.drawing/fill/forethemecolor/) { get; set; } | Hämtar eller ställer in ett ThemeColor-objekt som representerar förgrundsfärgen för fyllningen. |
| [ForeTintAndShade](../../aspose.words.drawing/fill/foretintandshade/) { get; set; } | Hämtar eller ställer in ett dubbelt värde som gör förgrundsfärgen ljusare eller mörkare. |
| [GradientAngle](../../aspose.words.drawing/fill/gradientangle/) { get; set; } | Hämtar eller ställer in vinkeln för gradientfyllningen. |
| [GradientStops](../../aspose.words.drawing/fill/gradientstops/) { get; } | Får en samling av[`GradientStop`](../gradientstop/) objekt för fill. |
| [GradientStyle](../../aspose.words.drawing/fill/gradientstyle/) { get; } | Hämtar gradientstilen[`GradientStyle`](../gradientstyle/) för fyllningen. |
| [GradientVariant](../../aspose.words.drawing/fill/gradientvariant/) { get; } | Hämtar gradientvarianten[`GradientVariant`](../gradientvariant/) för fyllningen. |
| [ImageBytes](../../aspose.words.drawing/fill/imagebytes/) { get; } | Hämtar råbyte för fyllningstexturen eller mönstret. |
| [Opacity](../../aspose.words.drawing/fill/opacity/) { get; set; } | Hämtar eller ställer in graden av opacitet för den angivna fyllningen som ett värde mellan 0,0 (clear) och 1,0 (opak). |
| [Pattern](../../aspose.words.drawing/fill/pattern/) { get; } | Får en[`PatternType`](../patterntype/) för fyllningen. |
| [PresetTexture](../../aspose.words.drawing/fill/presettexture/) { get; } | Får en[`PresetTexture`](../presettexture/) för fyllningen. |
| [RotateWithObject](../../aspose.words.drawing/fill/rotatewithobject/) { get; set; } | Hämtar eller ställer in om fyllningen roterar med det angivna objektet. |
| [TextureAlignment](../../aspose.words.drawing/fill/texturealignment/) { get; set; } | Hämtar eller ställer in justeringen för kakeltexturfyllning. |
| [Transparency](../../aspose.words.drawing/fill/transparency/) { get; set; } | Hämtar eller ställer in graden av transparens för den angivna fyllningen som ett värde mellan 0,0 (opak) och 1,0 (clear). |
| [Visible](../../aspose.words.drawing/fill/visible/) { get; set; } | Hämtar eller ställer in värde dvs`Sann` om formateringen som tillämpas på den här instansen är synlig. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [OneColorGradient](../../aspose.words.drawing/fill/onecolorgradient/#onecolorgradient)(GradientStyle, GradientVariant, double) | Ställer in den angivna fyllningen till en enfärgsgradient. |
| [OneColorGradient](../../aspose.words.drawing/fill/onecolorgradient/#onecolorgradient_1)(Color, GradientStyle, GradientVariant, double) | Ställer in den angivna fyllningen till en enfärgsgradient med den angivna färgen. |
| [Patterned](../../aspose.words.drawing/fill/patterned/#patterned)(PatternType) | Ställer in den angivna fyllningen till ett mönster. |
| [Patterned](../../aspose.words.drawing/fill/patterned/#patterned_1)(PatternType, Color, Color) | Ställer in den angivna fyllningen till ett mönster. |
| [PresetTextured](../../aspose.words.drawing/fill/presettextured/)(PresetTexture) | Ställer in fyllningen till en förinställd textur. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage)(byte[]) | Ändrar fyllningstypen till en bild. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage_1)(Stream) | Ändrar fyllningstypen till en bild. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage_2)(string) | Ändrar fyllningstypen till en bild. |
| [Solid](../../aspose.words.drawing/fill/solid/#solid)() | Ställer in fyllningen till en enhetlig färg. |
| [Solid](../../aspose.words.drawing/fill/solid/#solid_1)(Color) | Ställer in fyllningen till en specificerad enhetlig färg. |
| [TwoColorGradient](../../aspose.words.drawing/fill/twocolorgradient/#twocolorgradient)(GradientStyle, GradientVariant) | Ställer in den angivna fyllningen till en tvåfärgsgradient. |
| [TwoColorGradient](../../aspose.words.drawing/fill/twocolorgradient/#twocolorgradient_1)(Color, Color, GradientStyle, GradientVariant) | Ställer in den angivna fyllningen till en tvåfärgsgradient. |

### Anmärkningar

Använd[`Fill`](../shapebase/fill/) eller[`Fill`](../../aspose.words/font/fill/) egenskap för att komma åt fyllegenskaper för ett objekt. Du skapar inte instanser av`Fill` klass direkt.

### Exempel

Visar hur man fyller en form med enfärgad.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skriv lite text och täck den sedan med en flytande form.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// Använd egenskapen "StrokeColor" för att ställa in färgen på formens kontur.
shape.StrokeColor = Color.CadetBlue;

// Använd egenskapen "FillColor" för att ställa in färgen på formens insida.
shape.FillColor = Color.LightBlue;

// Egenskapen "Opacity" bestämmer hur transparent färgen är på en skala 0-1,
// där 1 är helt ogenomskinlig och 0 är osynlig.
// Formfyllningen är som standard helt ogenomskinlig, så vi kan inte se texten som denna form är ovanpå.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// Ställ in formfyllningsfärgens opacitet till ett lägre värde så att vi kan se texten under den.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### Se även

* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)


