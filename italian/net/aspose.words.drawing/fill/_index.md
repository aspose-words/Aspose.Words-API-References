---
title: Fill Class
linktitle: Fill
articleTitle: Fill
second_title: Aspose.Words per .NET
description: Esplora la classe Aspose.Words.Drawing.Fill per opzioni di formattazione di riempimento avanzate, migliorando senza sforzo il design e l'aspetto visivo del tuo documento.
type: docs
weight: 1270
url: /it/net/aspose.words.drawing/fill/
---
## Fill class

Rappresenta la formattazione di riempimento per un oggetto.

Per saperne di più, visita il[Lavorare con gli elementi grafici](https://docs.aspose.com/words/net/working-with-graphic-elements/) articolo di documentazione.

```csharp
public class Fill
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [BackColor](../../aspose.words.drawing/fill/backcolor/) { get; set; } | Ottiene o imposta un oggetto Color che rappresenta il colore di sfondo per il riempimento. |
| [BackThemeColor](../../aspose.words.drawing/fill/backthemecolor/) { get; set; } | Ottiene o imposta un oggetto ThemeColor che rappresenta il colore di sfondo per il riempimento. |
| [BackTintAndShade](../../aspose.words.drawing/fill/backtintandshade/) { get; set; } | Ottiene o imposta un valore double che schiarisce o scurisce il colore di sfondo. |
| [BaseForeColor](../../aspose.words.drawing/fill/baseforecolor/) { get; } | Ottiene un oggetto Color che rappresenta il colore di base in primo piano per fill senza modificatori. |
| [Color](../../aspose.words.drawing/fill/color/) { get; set; } | Ottiene o imposta un oggetto Color che rappresenta il colore di primo piano per il riempimento. |
| [FillType](../../aspose.words.drawing/fill/filltype/) { get; } | Ottiene un tipo di riempimento. |
| [ForeColor](../../aspose.words.drawing/fill/forecolor/) { get; set; } | Ottiene o imposta un oggetto Color che rappresenta il colore di primo piano per il riempimento. |
| [ForeThemeColor](../../aspose.words.drawing/fill/forethemecolor/) { get; set; } | Ottiene o imposta un oggetto ThemeColor che rappresenta il colore di primo piano per il riempimento. |
| [ForeTintAndShade](../../aspose.words.drawing/fill/foretintandshade/) { get; set; } | Ottiene o imposta un valore double che schiarisce o scurisce il colore di primo piano. |
| [GradientAngle](../../aspose.words.drawing/fill/gradientangle/) { get; set; } | Ottiene o imposta l'angolo del riempimento sfumato. |
| [GradientStops](../../aspose.words.drawing/fill/gradientstops/) { get; } | Ottiene una raccolta di[`GradientStop`](../gradientstop/) oggetti per il riempimento. |
| [GradientStyle](../../aspose.words.drawing/fill/gradientstyle/) { get; } | Ottiene lo stile del gradiente[`GradientStyle`](../gradientstyle/) per il riempimento. |
| [GradientVariant](../../aspose.words.drawing/fill/gradientvariant/) { get; } | Ottiene la variante del gradiente[`GradientVariant`](../gradientvariant/) per il riempimento. |
| [ImageBytes](../../aspose.words.drawing/fill/imagebytes/) { get; } | Ottiene i byte grezzi della texture o del motivo di riempimento. |
| [Opacity](../../aspose.words.drawing/fill/opacity/) { get; set; } | Ottiene o imposta il grado di opacità del riempimento specificato come valore compreso tra 0,0 (trasparente) e 1,0 (opaco). |
| [Pattern](../../aspose.words.drawing/fill/pattern/) { get; } | Ottiene un[`PatternType`](../patterntype/) per il riempimento. |
| [PresetTexture](../../aspose.words.drawing/fill/presettexture/) { get; } | Ottiene un[`PresetTexture`](../presettexture/) per il riempimento. |
| [RotateWithObject](../../aspose.words.drawing/fill/rotatewithobject/) { get; set; } | Ottiene o imposta se il riempimento ruota con l'oggetto specificato. |
| [TextureAlignment](../../aspose.words.drawing/fill/texturealignment/) { get; set; } | Ottiene o imposta l'allineamento per il riempimento della trama delle piastrelle. |
| [Transparency](../../aspose.words.drawing/fill/transparency/) { get; set; } | Ottiene o imposta il grado di trasparenza del riempimento specificato come valore compreso tra 0,0 (opaco) e 1,0 (trasparente). |
| [Visible](../../aspose.words.drawing/fill/visible/) { get; set; } | Ottiene o imposta il valore che è`VERO` se la formattazione applicata a questa istanza è visibile. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [OneColorGradient](../../aspose.words.drawing/fill/onecolorgradient/#onecolorgradient)(*[GradientStyle](../gradientstyle/), [GradientVariant](../gradientvariant/), double*) | Imposta il riempimento specificato su un gradiente di un solo colore. |
| [OneColorGradient](../../aspose.words.drawing/fill/onecolorgradient/#onecolorgradient_1)(*Color, [GradientStyle](../gradientstyle/), [GradientVariant](../gradientvariant/), double*) | Imposta il riempimento specificato su un gradiente monocolore utilizzando il colore specificato. |
| [Patterned](../../aspose.words.drawing/fill/patterned/#patterned)(*[PatternType](../patterntype/)*) | Imposta il riempimento specificato su un motivo. |
| [Patterned](../../aspose.words.drawing/fill/patterned/#patterned_1)(*[PatternType](../patterntype/), Color, Color*) | Imposta il riempimento specificato su un motivo. |
| [PresetTextured](../../aspose.words.drawing/fill/presettextured/)(*[PresetTexture](../presettexture/)*) | Imposta il riempimento su una texture preimpostata. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage)(*byte[]*) | Cambia il tipo di riempimento in immagine singola. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage_1)(*Stream*) | Cambia il tipo di riempimento in immagine singola. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage_2)(*string*) | Cambia il tipo di riempimento in immagine singola. |
| [Solid](../../aspose.words.drawing/fill/solid/#solid)() | Imposta il riempimento su un colore uniforme. |
| [Solid](../../aspose.words.drawing/fill/solid/#solid_1)(*Color*) | Imposta il riempimento su un colore uniforme specificato. |
| [TwoColorGradient](../../aspose.words.drawing/fill/twocolorgradient/#twocolorgradient)(*[GradientStyle](../gradientstyle/), [GradientVariant](../gradientvariant/)*) | Imposta il riempimento specificato su un gradiente a due colori. |
| [TwoColorGradient](../../aspose.words.drawing/fill/twocolorgradient/#twocolorgradient_1)(*Color, Color, [GradientStyle](../gradientstyle/), [GradientVariant](../gradientvariant/)*) | Imposta il riempimento specificato su un gradiente a due colori. |

## Osservazioni

Utilizzare il[`Fill`](../shapebase/fill/) O[`Fill`](../../aspose.words/font/fill/) proprietà per accedere alle proprietà di riempimento di un oggetto. Non si creano istanze di`Fill` classe direttamente.

## Esempi

Mostra come riempire una forma con un colore pieno.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Scrivi del testo e poi coprilo con una forma fluttuante.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// Utilizzare la proprietà "StrokeColor" per impostare il colore del contorno della forma.
shape.StrokeColor = Color.CadetBlue;

// Utilizzare la proprietà "FillColor" per impostare il colore dell'area interna della forma.
shape.FillColor = Color.LightBlue;

// La proprietà "Opacità" determina quanto è trasparente il colore su una scala da 0 a 1,
// dove 1 è completamente opaco e 0 è invisibile.
// Per impostazione predefinita, il riempimento della forma è completamente opaco, quindi non possiamo vedere il testo su cui si trova questa forma.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// Imposta l'opacità del colore di riempimento della forma su un valore più basso, in modo da poter vedere il testo sottostante.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)
