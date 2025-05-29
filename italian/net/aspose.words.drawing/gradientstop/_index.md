---
title: GradientStop Class
linktitle: GradientStop
articleTitle: GradientStop
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Drawing.GradientStop, la soluzione per creare sfumature straordinarie con interruzioni personalizzabili per migliorare la visualizzazione dei documenti.
type: docs
weight: 1310
url: /it/net/aspose.words.drawing/gradientstop/
---
## GradientStop class

Rappresenta un'interruzione del gradiente.

Per saperne di più, visita il[Lavorare con gli elementi grafici](https://docs.aspose.com/words/net/working-with-graphic-elements/) articolo di documentazione.

```csharp
public class GradientStop
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [GradientStop](gradientstop/#constructor)(*Color, double*) | Inizializza una nuova istanza di`GradientStop` classe. |
| [GradientStop](gradientstop/#constructor_1)(*Color, double, double*) | Inizializza una nuova istanza di`GradientStop` classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [BaseColor](../../aspose.words.drawing/gradientstop/basecolor/) { get; } | Ottiene un valore che rappresenta il colore del gradiente senza modificatori. |
| [Color](../../aspose.words.drawing/gradientstop/color/) { get; set; } | Ottiene o imposta un valore che rappresenta il colore del punto di interruzione del gradiente. |
| [Position](../../aspose.words.drawing/gradientstop/position/) { get; set; } | Ottiene o imposta un valore che rappresenta la posizione di una fermata all'interno del gradiente espresso come percentuale nell'intervallo da 0,0 a 1,0. |
| [Transparency](../../aspose.words.drawing/gradientstop/transparency/) { get; set; } | Ottiene o imposta un valore che rappresenta la trasparenza del riempimento sfumato espresso come percentuale nell'intervallo da 0,0 a 1,0. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Remove](../../aspose.words.drawing/gradientstop/remove/)() | Rimuove l'interruzione del gradiente dal genitore[`GradientStopCollection`](../gradientstopcollection/) . |

## Esempi

Mostra come aggiungere interruzioni di sfumatura al riempimento sfumato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
shape.Fill.TwoColorGradient(Color.Green, Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2);

// Ottieni la raccolta di interruzioni del gradiente.
GradientStopCollection gradientStops = shape.Fill.GradientStops;

// Modifica la prima interruzione del gradiente.
gradientStops[0].Color = Color.Aqua;
gradientStops[0].Position = 0.1;
gradientStops[0].Transparency = 0.25;

// Aggiunge una nuova interruzione del gradiente alla fine della raccolta.
GradientStop gradientStop = new GradientStop(Color.Brown, 0.5);
gradientStops.Add(gradientStop);

// Rimuovi l'interruzione del gradiente all'indice 1.
gradientStops.RemoveAt(1);
// E inserisci un nuovo punto di interruzione del gradiente allo stesso indice 1.
gradientStops.Insert(1, new GradientStop(Color.Chocolate, 0.75, 0.3));

// Rimuove l'ultima interruzione del gradiente nella raccolta.
gradientStop = gradientStops[2];
gradientStops.Remove(gradientStop);

Assert.AreEqual(2, gradientStops.Count);

Assert.AreEqual(Color.FromArgb(255, 0, 255, 255), gradientStops[0].BaseColor);
Assert.AreEqual(Color.Aqua.ToArgb(), gradientStops[0].Color.ToArgb());
Assert.AreEqual(0.1d, gradientStops[0].Position, 0.01d);
Assert.AreEqual(0.25d, gradientStops[0].Transparency, 0.01d);

Assert.AreEqual(Color.Chocolate.ToArgb(), gradientStops[1].Color.ToArgb());
Assert.AreEqual(0.75d, gradientStops[1].Position, 0.01d);
Assert.AreEqual(0.3d, gradientStops[1].Transparency, 0.01d);

// Utilizzare l'opzione di conformità per definire la forma utilizzando DML
// se si desidera ottenere la proprietà "GradientStops" dopo il salvataggio del documento.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientStops.docx", saveOptions);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)
