---
title: GradientStopCollection.Remove
second_title: Aspose.Words per .NET API Reference
description: GradientStopCollection metodo. Rimuove uno specificatoGradientStop dalla collezione.
type: docs
weight: 60
url: /it/net/aspose.words.drawing/gradientstopcollection/remove/
---
## GradientStopCollection.Remove method

Rimuove uno specificato[`GradientStop`](../../gradientstop/) dalla collezione.

```csharp
public bool Remove(GradientStop gradientStop)
```

### Valore di ritorno

Vero se l'arresto del gradiente è stato rimosso con successo, altrimenti falso.

### Esempi

Mostra come aggiungere interruzioni di sfumatura al riempimento sfumato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
shape.Fill.TwoColorGradient(Color.Green, Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2);

// Ottieni la raccolta delle interruzioni del gradiente.
GradientStopCollection gradientStops = shape.Fill.GradientStops;

// Cambia la prima fermata del gradiente.
gradientStops[0].Color = Color.Aqua;
gradientStops[0].Position = 0.1;
gradientStops[0].Transparency = 0.25;

// Aggiunge una nuova interruzione del gradiente alla fine della raccolta.
GradientStop gradientStop = new GradientStop(Color.Brown, 0.5);
gradientStops.Add(gradientStop);

// Rimuove l'arresto del gradiente all'indice 1.
gradientStops.RemoveAt(1);
// E inserisci una nuova fermata del gradiente allo stesso indice 1.
gradientStops.Insert(1, new GradientStop(Color.Chocolate, 0.75, 0.3));

// Rimuovi l'ultima fermata del gradiente nella raccolta.
gradientStop = gradientStops[2];
gradientStops.Remove(gradientStop);

Assert.AreEqual(2, gradientStops.Count);

Assert.AreEqual(Color.Aqua.ToArgb(), gradientStops[0].Color.ToArgb());
Assert.AreEqual(0.1d, gradientStops[0].Position, 0.01d);
Assert.AreEqual(0.25d, gradientStops[0].Transparency, 0.01d);

Assert.AreEqual(Color.Chocolate.ToArgb(), gradientStops[1].Color.ToArgb());
Assert.AreEqual(0.75d, gradientStops[1].Position, 0.01d);
Assert.AreEqual(0.3d, gradientStops[1].Transparency, 0.01d);

// Usa l'opzione di conformità per definire la forma usando DML
// se vuoi ottenere la proprietà "GradientStops" dopo il salvataggio del documento.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientStops.docx", saveOptions);
```

### Guarda anche

* class [GradientStop](../../gradientstop/)
* class [GradientStopCollection](../)
* spazio dei nomi [Aspose.Words.Drawing](../../gradientstopcollection/)
* assemblea [Aspose.Words](../../../)


