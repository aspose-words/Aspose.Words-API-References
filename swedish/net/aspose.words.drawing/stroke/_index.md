---
title: Stroke Class
linktitle: Stroke
articleTitle: Stroke
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Drawing.Stroke för att förbättra dina former med anpassningsbara penseldrag och enkelt ge dina dokument en professionell touch.
type: docs
weight: 1720
url: /sv/net/aspose.words.drawing/stroke/
---
## Stroke class

Definierar ett streck för en form.

För att lära dig mer, besök[Arbeta med former](https://docs.aspose.com/words/net/working-with-shapes/) dokumentationsartikel.

```csharp
public class Stroke
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [BackColor](../../aspose.words.drawing/stroke/backcolor/) { get; set; } | Hämtar eller ställer in bakgrundsfärgen för linjen. |
| [BackThemeColor](../../aspose.words.drawing/stroke/backthemecolor/) { get; set; } | Hämtar eller ställer in ett ThemeColor-objekt som representerar streckets bakgrundsfärg. |
| [BackTintAndShade](../../aspose.words.drawing/stroke/backtintandshade/) { get; set; } | Hämtar eller ställer in ett dubbelvärde som ljusar eller mörkar upp linjens bakgrundsfärg. |
| [BaseForeColor](../../aspose.words.drawing/stroke/baseforecolor/) { get; } | Hämtar den grundläggande förgrundsfärgen för linjen utan några modifierare. |
| [Color](../../aspose.words.drawing/stroke/color/) { get; set; } | Definierar färgen på ett streck. |
| [Color2](../../aspose.words.drawing/stroke/color2/) { get; set; } | Definierar en andra färg för ett streck. |
| [DashStyle](../../aspose.words.drawing/stroke/dashstyle/) { get; set; } | Anger punkt- och streckmönstret för ett streck. |
| [EndArrowLength](../../aspose.words.drawing/stroke/endarrowlength/) { get; set; } | Definierar pilspetslängden för slutet av ett penseldrag. |
| [EndArrowType](../../aspose.words.drawing/stroke/endarrowtype/) { get; set; } | Definierar pilspetsen för slutet av ett penseldrag. |
| [EndArrowWidth](../../aspose.words.drawing/stroke/endarrowwidth/) { get; set; } | Definierar pilspetsbredden för slutet av ett penseldrag. |
| [EndCap](../../aspose.words.drawing/stroke/endcap/) { get; set; } | Definierar ändstilen för slutet av ett penseldrag. |
| [Fill](../../aspose.words.drawing/stroke/fill/) { get; } | Hämtar fyllningsformatering för`Stroke` . |
| [ForeColor](../../aspose.words.drawing/stroke/forecolor/) { get; set; } | Hämtar eller ställer in förgrundsfärgen för linjen. |
| [ForeThemeColor](../../aspose.words.drawing/stroke/forethemecolor/) { get; set; } | Hämtar eller ställer in ett ThemeColor-objekt som representerar streckets förgrundsfärg. |
| [ForeTintAndShade](../../aspose.words.drawing/stroke/foretintandshade/) { get; set; } | Hämtar eller ställer in ett dubbelvärde som ljusar eller mörkar upp linjens förgrundsfärg. |
| [ImageBytes](../../aspose.words.drawing/stroke/imagebytes/) { get; } | Definierar bilden för en linjebild eller mönsterfyllning. |
| [JoinStyle](../../aspose.words.drawing/stroke/joinstyle/) { get; set; } | Definierar kopplingsstilen för en polylinje. |
| [LineStyle](../../aspose.words.drawing/stroke/linestyle/) { get; set; } | Definierar linjestilen för linjen. |
| [On](../../aspose.words.drawing/stroke/on/) { get; set; } | Definierar om banan ska vara linjerad. |
| [Opacity](../../aspose.words.drawing/stroke/opacity/) { get; set; } | Definierar mängden genomskinlighet för ett penseldrag. Giltigt intervall är från 0 till 1. |
| [StartArrowLength](../../aspose.words.drawing/stroke/startarrowlength/) { get; set; } | Definierar pilspetslängden för början av ett streck. |
| [StartArrowType](../../aspose.words.drawing/stroke/startarrowtype/) { get; set; } | Definierar pilspetsen för början av ett streck. |
| [StartArrowWidth](../../aspose.words.drawing/stroke/startarrowwidth/) { get; set; } | Definierar pilspetsbredden för början av ett streck. |
| [Transparency](../../aspose.words.drawing/stroke/transparency/) { get; set; } | Hämtar eller ställer in ett värde mellan 0,0 (ogenomskinlig) och 1,0 (klar) som representerar graden av genomskinlighet för linjen. |
| [Visible](../../aspose.words.drawing/stroke/visible/) { get; set; } | Hämtar eller anger en flagga som anger om linjen är synlig. |
| [Weight](../../aspose.words.drawing/stroke/weight/) { get; set; } | Definierar penselns tjocklek som stryker längs en forms bana i punkter. |

## Anmärkningar

Använd[`Stroke`](../shape/stroke/)egenskap för att komma åt linjeegenskaper för en form. Du skapar inte instanser av`Stroke` klass direkt.

## Exempel

Visar hur man ändrar penseldragsegenskaper.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 200, 200, WrapType.None);

// Grundläggande former, som rektangeln, har två synliga delar.
// 1 - Fyllningen, som gäller området inom formens kontur:
shape.Fill.ForeColor = Color.White;

// 2 - Linjen, som markerar formens konturer:
// Ändra olika egenskaper för den här formens linje.
Stroke stroke = shape.Stroke;
stroke.On = true;
stroke.Weight = 5;
stroke.Color = Color.Red;
stroke.DashStyle = DashStyle.ShortDashDotDot;
stroke.JoinStyle = JoinStyle.Miter;
stroke.EndCap = EndCap.Square;
stroke.LineStyle = ShapeLineStyle.Triple;
stroke.Fill.TwoColorGradient(Color.Red, Color.Blue, GradientStyle.Vertical, GradientVariant.Variant1);

doc.Save(ArtifactsDir + "Shape.Stroke.docx");
```

### Se även

* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
