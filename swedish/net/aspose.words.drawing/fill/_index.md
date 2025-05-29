---
title: Fill Class
linktitle: Fill
articleTitle: Fill
second_title: Aspose.Words för .NET
description: Utforska klassen Aspose.Words.Drawing.Fill för avancerade alternativ för fyllningsformatering, vilket enkelt förbättrar din dokumentdesign och visuella attraktionskraft.
type: docs
weight: 1270
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
| [BackColor](../../aspose.words.drawing/fill/backcolor/) { get; set; } | Hämtar eller ställer in ett Color-objekt som representerar bakgrundsfärgen för fyllningen. |
| [BackThemeColor](../../aspose.words.drawing/fill/backthemecolor/) { get; set; } | Hämtar eller ställer in ett ThemeColor-objekt som representerar bakgrundsfärgen för fyllningen. |
| [BackTintAndShade](../../aspose.words.drawing/fill/backtintandshade/) { get; set; } | Hämtar eller ställer in ett dubbelt värde som ljusar eller mörkar upp bakgrundsfärgen. |
| [BaseForeColor](../../aspose.words.drawing/fill/baseforecolor/) { get; } | Hämtar ett Color-objekt som representerar basförgrundsfärgen för fill utan några modifierare. |
| [Color](../../aspose.words.drawing/fill/color/) { get; set; } | Hämtar eller ställer in ett Color-objekt som representerar förgrundsfärgen för fyllningen. |
| [FillType](../../aspose.words.drawing/fill/filltype/) { get; } | Hämtar en fyllningstyp. |
| [ForeColor](../../aspose.words.drawing/fill/forecolor/) { get; set; } | Hämtar eller ställer in ett Color-objekt som representerar förgrundsfärgen för fyllningen. |
| [ForeThemeColor](../../aspose.words.drawing/fill/forethemecolor/) { get; set; } | Hämtar eller ställer in ett ThemeColor-objekt som representerar förgrundsfärgen för fyllningen. |
| [ForeTintAndShade](../../aspose.words.drawing/fill/foretintandshade/) { get; set; } | Hämtar eller ställer in ett dubbelvärde som ljusar eller mörkar förgrundsfärgen. |
| [GradientAngle](../../aspose.words.drawing/fill/gradientangle/) { get; set; } | Hämtar eller ställer in vinkeln på gradientfyllningen. |
| [GradientStops](../../aspose.words.drawing/fill/gradientstops/) { get; } | Hämtar en samling av[`GradientStop`](../gradientstop/) objekt för fyllningen. |
| [GradientStyle](../../aspose.words.drawing/fill/gradientstyle/) { get; } | Hämtar gradientstilen[`GradientStyle`](../gradientstyle/) för fyllningen. |
| [GradientVariant](../../aspose.words.drawing/fill/gradientvariant/) { get; } | Hämtar gradientvarianten[`GradientVariant`](../gradientvariant/) för fyllningen. |
| [ImageBytes](../../aspose.words.drawing/fill/imagebytes/) { get; } | Hämtar råa byte av fyllnadstexturen eller mönstret. |
| [Opacity](../../aspose.words.drawing/fill/opacity/) { get; set; } | Hämtar eller ställer in graden av opacitet för den angivna fyllningen som ett värde mellan 0,0 (klar) och 1,0 (ogenomskinlig). |
| [Pattern](../../aspose.words.drawing/fill/pattern/) { get; } | Får en[`PatternType`](../patterntype/) för fyllningen. |
| [PresetTexture](../../aspose.words.drawing/fill/presettexture/) { get; } | Får en[`PresetTexture`](../presettexture/) för fyllningen. |
| [RotateWithObject](../../aspose.words.drawing/fill/rotatewithobject/) { get; set; } | Hämtar eller anger om fyllningen roterar med det angivna objektet. |
| [TextureAlignment](../../aspose.words.drawing/fill/texturealignment/) { get; set; } | Hämtar eller ställer in justeringen för fyllning av kakeltextur. |
| [Transparency](../../aspose.words.drawing/fill/transparency/) { get; set; } | Hämtar eller ställer in graden av genomskinlighet för den angivna fyllningen som ett värde mellan 0,0 (ogenomskinlig) och 1,0 (klar). |
| [Visible](../../aspose.words.drawing/fill/visible/) { get; set; } | Hämtar eller ställer in ett värde som är`sann` om formateringen som tillämpats på den här instansen är synlig. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [OneColorGradient](../../aspose.words.drawing/fill/onecolorgradient/#onecolorgradient)(*[GradientStyle](../gradientstyle/), [GradientVariant](../gradientvariant/), double*) | Ställer in den angivna fyllningen till en enfärgad gradient. |
| [OneColorGradient](../../aspose.words.drawing/fill/onecolorgradient/#onecolorgradient_1)(*Color, [GradientStyle](../gradientstyle/), [GradientVariant](../gradientvariant/), double*) | Ställer in den angivna fyllningen till en enfärgad gradient med den angivna färgen. |
| [Patterned](../../aspose.words.drawing/fill/patterned/#patterned)(*[PatternType](../patterntype/)*) | Ställer in den angivna fyllningen till ett mönster. |
| [Patterned](../../aspose.words.drawing/fill/patterned/#patterned_1)(*[PatternType](../patterntype/), Color, Color*) | Ställer in den angivna fyllningen till ett mönster. |
| [PresetTextured](../../aspose.words.drawing/fill/presettextured/)(*[PresetTexture](../presettexture/)*) | Ställer in fyllningen till en förinställd textur. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage)(*byte[]*) | Ändrar fyllningstypen till en enda bild. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage_1)(*Stream*) | Ändrar fyllningstypen till en enda bild. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage_2)(*string*) | Ändrar fyllningstypen till en enda bild. |
| [Solid](../../aspose.words.drawing/fill/solid/#solid)() | Ställer in fyllningen till en enhetlig färg. |
| [Solid](../../aspose.words.drawing/fill/solid/#solid_1)(*Color*) | Ställer in fyllningen till en angiven enhetlig färg. |
| [TwoColorGradient](../../aspose.words.drawing/fill/twocolorgradient/#twocolorgradient)(*[GradientStyle](../gradientstyle/), [GradientVariant](../gradientvariant/)*) | Ställer in den angivna fyllningen till en tvåfärgad gradient. |
| [TwoColorGradient](../../aspose.words.drawing/fill/twocolorgradient/#twocolorgradient_1)(*Color, Color, [GradientStyle](../gradientstyle/), [GradientVariant](../gradientvariant/)*) | Ställer in den angivna fyllningen till en tvåfärgad gradient. |

## Anmärkningar

Använd[`Fill`](../shapebase/fill/) eller[`Fill`](../../aspose.words/font/fill/) egenskap för att komma åt fyllningsegenskaper för ett objekt. Du skapar inte instanser av`Fill` klass direkt.

## Exempel

Visar hur man fyller en form med en helfärg.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skriv lite text och täck den sedan med en flytande form.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// Använd egenskapen "StrokeColor" för att ange färgen på formens kontur.
shape.StrokeColor = Color.CadetBlue;

// Använd egenskapen "FillColor" för att ange färgen på formens insida.
shape.FillColor = Color.LightBlue;

// Egenskapen "Opacitet" avgör hur transparent färgen är på en skala från 0 till 1,
// där 1 är helt ogenomskinlig och 0 är osynlig.
// Formfyllningen är som standard helt ogenomskinlig, så vi kan inte se texten som formen ligger ovanpå.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// Ställ in fyllningsfärgens opacitet till ett lägre värde så att vi kan se texten under den.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### Se även

* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
