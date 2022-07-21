---
title: GradientStop
second_title: Aspose.Words per .NET API Reference
description: Inizializza una nuova istanza diGradientStopaspose.words.drawing/gradientstop classe.
type: docs
weight: 10
url: /it/net/aspose.words.drawing/gradientstop/gradientstop/
---
## GradientStop(Color, double) {#constructor}

Inizializza una nuova istanza di[`GradientStop`](../../gradientstop) classe.

```csharp
public GradientStop(Color color, double position)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| color | Color | Rappresenta il colore dell'interruzione del gradiente. |
| position | Double | Rappresenta la posizione di uno stop entro il gradiente espresso in percentuale nell'intervallo da 0,0 a 1,0. |

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

* class [GradientStop](../../gradientstop)
* spazio dei nomi [Aspose.Words.Drawing](../../gradientstop)
* assemblea [Aspose.Words](../../../)

---

## GradientStop(Color, double, double) {#constructor_1}

Inizializza una nuova istanza di[`GradientStop`](../../gradientstop) classe.

```csharp
public GradientStop(Color color, double position, double transparency)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| color | Color | Rappresenta il colore dell'interruzione del gradiente. |
| position | Double | Rappresenta la posizione di uno stop entro il gradiente espresso in percentuale nell'intervallo da 0,0 a 1,0. |
| transparency | Double | Rappresenta la trasparenza di una sosta entro il gradiente espresso in percentuale nell'intervallo da 0,0 a 1,0. |

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

* class [GradientStop](../../gradientstop)
* spazio dei nomi [Aspose.Words.Drawing](../../gradientstop)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
