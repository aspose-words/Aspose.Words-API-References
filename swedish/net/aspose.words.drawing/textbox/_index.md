---
title: TextBox Class
linktitle: TextBox
articleTitle: TextBox
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Drawing.TextBox för att enkelt anpassa textvisningen i former, vilket förbättrar dokumentets visuella attraktionskraft och funktionalitet.
type: docs
weight: 1730
url: /sv/net/aspose.words.drawing/textbox/
---
## TextBox class

Definierar attribut som anger hur en text visas inuti en form.

För att lära dig mer, besök[Arbeta med former](https://docs.aspose.com/words/net/working-with-shapes/) dokumentationsartikel.

```csharp
public class TextBox
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [FitShapeToText](../../aspose.words.drawing/textbox/fitshapetotext/) { get; set; } | Avgör om Microsoft Word ska utöka formen så att den passar text. |
| [InternalMarginBottom](../../aspose.words.drawing/textbox/internalmarginbottom/) { get; set; } | Anger den inre nedre marginalen i punkter för en form. |
| [InternalMarginLeft](../../aspose.words.drawing/textbox/internalmarginleft/) { get; set; } | Anger den inre vänstra marginalen i punkter för en form. |
| [InternalMarginRight](../../aspose.words.drawing/textbox/internalmarginright/) { get; set; } | Anger den inre högra marginalen i punkter för en form. |
| [InternalMarginTop](../../aspose.words.drawing/textbox/internalmargintop/) { get; set; } | Anger den inre övre marginalen i punkter för en form. |
| [LayoutFlow](../../aspose.words.drawing/textbox/layoutflow/) { get; set; } | Bestämmer flödet för textlayouten i en form. |
| [Next](../../aspose.words.drawing/textbox/next/) { get; set; } | Returnerar eller anger en`TextBox` som representerar nästa`TextBox` en sekvens av former. |
| [NoTextRotation](../../aspose.words.drawing/textbox/notextrotation/) { get; set; } | Hämtar eller ställer in ett booleskt värde som anger att någon av texterna i textrutan inte ska rotera när formen roteras. |
| [Parent](../../aspose.words.drawing/textbox/parent/) { get; } | Hämtar en förälderform för`TextBox` . |
| [Previous](../../aspose.words.drawing/textbox/previous/) { get; } | Returnerar en`TextBox` som representerar det föregående`TextBox` en sekvens av former. |
| [TextBoxWrapMode](../../aspose.words.drawing/textbox/textboxwrapmode/) { get; set; } | Bestämmer hur text radbryts inuti en form. |
| [VerticalAnchor](../../aspose.words.drawing/textbox/verticalanchor/) { get; set; } | Anger den vertikala justeringen av texten inom en form. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [BreakForwardLink](../../aspose.words.drawing/textbox/breakforwardlink/)() | Bryter länken till nästa`TextBox` . |
| [IsValidLinkTarget](../../aspose.words.drawing/textbox/isvalidlinktarget/)(*TextBox*) | Avgör om detta`TextBox` kan kopplas till målet`TextBox` . |

## Anmärkningar

Använd[`TextBox`](../shape/textbox/) egenskap för att komma åt textegenskaper för en form. Du skapar inte instanser av`TextBox` klass direkt.

## Exempel

Visar hur man ställer in interna marginaler för en textruta.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga ytterligare en textruta med specifika marginaler.
Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 100, 100);
TextBox textBox = textBoxShape.TextBox;
textBox.InternalMarginTop = 15;
textBox.InternalMarginBottom = 15;
textBox.InternalMarginLeft = 15;
textBox.InternalMarginRight = 15;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text placed according to textbox margins.");

doc.Save(ArtifactsDir + "Shape.TextBoxMargins.docx");
```

Visar hur man ställer in textens orientering inuti en textruta.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Flytta dokumentbyggaren till textrutan och lägg till text.
builder.MoveTo(textBoxShape.LastParagraph);
builder.Writeln("Hello world!");
builder.Write("Hello again!");

// Ställ in egenskapen "LayoutFlow" för att ange en orientering för textinnehållet i den här textrutan.
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

Visar hur man får en textruta att ändra storlek så att den får plats med innehållet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Tillämpa dessa värden på båda dessa medlemmar för att få den överordnade formen att passa
// tätt runt textinnehållet, utan att tänka på de dimensioner vi har angett.
textBox.FitShapeToText = true;
textBox.TextBoxWrapMode = TextBoxWrapMode.None;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text fit tightly inside textbox.");

doc.Save(ArtifactsDir + "Shape.TextBoxFitShapeToText.docx");
```

### Se även

* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
