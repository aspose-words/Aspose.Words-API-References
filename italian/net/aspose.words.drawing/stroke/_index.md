---
title: Stroke Class
linktitle: Stroke
articleTitle: Stroke
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Drawing.Stroke per migliorare le tue forme con tratti personalizzabili, aggiungendo senza sforzo un tocco professionale ai tuoi documenti.
type: docs
weight: 1720
url: /it/net/aspose.words.drawing/stroke/
---
## Stroke class

Definisce un tratto per una forma.

Per saperne di più, visita il[Lavorare con le forme](https://docs.aspose.com/words/net/working-with-shapes/) articolo di documentazione.

```csharp
public class Stroke
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [BackColor](../../aspose.words.drawing/stroke/backcolor/) { get; set; } | Ottiene o imposta il colore di sfondo del tratto. |
| [BackThemeColor](../../aspose.words.drawing/stroke/backthemecolor/) { get; set; } | Ottiene o imposta un oggetto ThemeColor che rappresenta il colore di sfondo del tratto. |
| [BackTintAndShade](../../aspose.words.drawing/stroke/backtintandshade/) { get; set; } | Ottiene o imposta un valore double che schiarisce o scurisce il colore di sfondo del tratto. |
| [BaseForeColor](../../aspose.words.drawing/stroke/baseforecolor/) { get; } | Ottiene il colore di base del primo piano del tratto senza modificatori. |
| [Color](../../aspose.words.drawing/stroke/color/) { get; set; } | Definisce il colore di un tratto. |
| [Color2](../../aspose.words.drawing/stroke/color2/) { get; set; } | Definisce un secondo colore per un tratto. |
| [DashStyle](../../aspose.words.drawing/stroke/dashstyle/) { get; set; } | Specifica il modello di punti e trattini per un tratto. |
| [EndArrowLength](../../aspose.words.drawing/stroke/endarrowlength/) { get; set; } | Definisce la lunghezza della punta della freccia per la fine di un tratto. |
| [EndArrowType](../../aspose.words.drawing/stroke/endarrowtype/) { get; set; } | Definisce la punta della freccia per la fine di un tratto. |
| [EndArrowWidth](../../aspose.words.drawing/stroke/endarrowwidth/) { get; set; } | Definisce la larghezza della punta della freccia per la fine di un tratto. |
| [EndCap](../../aspose.words.drawing/stroke/endcap/) { get; set; } | Definisce lo stile del tappo per la fine di un tratto. |
| [Fill](../../aspose.words.drawing/stroke/fill/) { get; } | Ottiene la formattazione di riempimento per il`Stroke` . |
| [ForeColor](../../aspose.words.drawing/stroke/forecolor/) { get; set; } | Ottiene o imposta il colore di primo piano del tratto. |
| [ForeThemeColor](../../aspose.words.drawing/stroke/forethemecolor/) { get; set; } | Ottiene o imposta un oggetto ThemeColor che rappresenta il colore di primo piano del tratto. |
| [ForeTintAndShade](../../aspose.words.drawing/stroke/foretintandshade/) { get; set; } | Ottiene o imposta un valore double che schiarisce o scurisce il colore di primo piano del tratto. |
| [ImageBytes](../../aspose.words.drawing/stroke/imagebytes/) { get; } | Definisce l'immagine per un'immagine di tratto o un riempimento a motivo. |
| [JoinStyle](../../aspose.words.drawing/stroke/joinstyle/) { get; set; } | Definisce lo stile di unione di una polilinea. |
| [LineStyle](../../aspose.words.drawing/stroke/linestyle/) { get; set; } | Definisce lo stile della linea del tratto. |
| [On](../../aspose.words.drawing/stroke/on/) { get; set; } | Definisce se il percorso verrà tracciato. |
| [Opacity](../../aspose.words.drawing/stroke/opacity/) { get; set; } | Definisce il grado di trasparenza di un tratto. L'intervallo valido è compreso tra 0 e 1. |
| [StartArrowLength](../../aspose.words.drawing/stroke/startarrowlength/) { get; set; } | Definisce la lunghezza della punta della freccia per l'inizio di un tratto. |
| [StartArrowType](../../aspose.words.drawing/stroke/startarrowtype/) { get; set; } | Definisce la punta della freccia per l'inizio di un tratto. |
| [StartArrowWidth](../../aspose.words.drawing/stroke/startarrowwidth/) { get; set; } | Definisce la larghezza della punta della freccia per l'inizio di un tratto. |
| [Transparency](../../aspose.words.drawing/stroke/transparency/) { get; set; } | Ottiene o imposta un valore compreso tra 0,0 (opaco) e 1,0 (trasparente) che rappresenta il grado di trasparenza del tratto. |
| [Visible](../../aspose.words.drawing/stroke/visible/) { get; set; } | Ottiene o imposta un flag che indica se il tratto è visibile. |
| [Weight](../../aspose.words.drawing/stroke/weight/) { get; set; } | Definisce lo spessore del pennello che traccia il percorso di una forma in punti. |

## Osservazioni

Utilizzare il[`Stroke`](../shape/stroke/)proprietà per accedere alle proprietà del tratto di una forma. Non si creano istanze di`Stroke` classe direttamente.

## Esempi

Mostra come modificare le proprietà del tratto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 200, 200, WrapType.None);

// Le forme base, come il rettangolo, hanno due parti visibili.
// 1 - Il riempimento, che si applica all'area all'interno del contorno della forma:
shape.Fill.ForeColor = Color.White;

// 2 - Il tratto, che segna il contorno della forma:
// Modifica varie proprietà del tratto di questa forma.
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

### Guarda anche

* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)
