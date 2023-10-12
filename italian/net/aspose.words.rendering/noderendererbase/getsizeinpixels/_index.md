---
title: NodeRendererBase.GetSizeInPixels
second_title: Aspose.Words per .NET API Reference
description: NodeRendererBase metodo. Calcola la dimensione della forma in pixel per un fattore di zoom e una risoluzione specificati.
type: docs
weight: 60
url: /it/net/aspose.words.rendering/noderendererbase/getsizeinpixels/
---
## GetSizeInPixels(float, float) {#getsizeinpixels}

Calcola la dimensione della forma in pixel per un fattore di zoom e una risoluzione specificati.

```csharp
public Size GetSizeInPixels(float scale, float dpi)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| scale | Single | Il fattore di zoom (1,0 è 100%). |
| dpi | Single | La risoluzione (orizzontale e verticale) per convertire da punti a pixel (punti per pollice). |

### Valore di ritorno

La dimensione della forma in pixel.

### Osservazioni

Questo metodo converte[`SizeInPoints`](../sizeinpoints/) nella dimensione in pixel ed è utile quando vuoi creare una bitmap per rendere ordinatamente la forma sulla bitmap.

### Esempi

Mostra come misurare e ridimensionare le forme.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);
OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

// Verifica la dimensione dell'immagine che l'oggetto OfficeMath creerà quando ne eseguiremo il rendering.
Assert.AreEqual(119.0f, renderer.SizeInPoints.Width, 0.2f);
Assert.AreEqual(13.0f, renderer.SizeInPoints.Height, 0.1f);

Assert.AreEqual(119.0f, renderer.BoundsInPoints.Width, 0.2f);
Assert.AreEqual(13.0f, renderer.BoundsInPoints.Height, 0.1f);

// Le forme con parti trasparenti possono contenere valori diversi nelle proprietà "OpaqueBoundsInPoints".
Assert.AreEqual(119.0f, renderer.OpaqueBoundsInPoints.Width, 0.2f);
Assert.AreEqual(14.2f, renderer.OpaqueBoundsInPoints.Height, 0.1f);

// Ottieni la dimensione della forma in pixel, con ridimensionamento lineare a un DPI specifico.
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(18, bounds.Height);

// Ottieni la dimensione della forma in pixel, ma con un DPI diverso per le dimensioni orizzontale e verticale.
bounds = renderer.GetBoundsInPixels(1.0f, 96.0f, 150.0f);
Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(28, bounds.Height);

// Anche qui i limiti opachi possono variare.
bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(18, bounds.Height);

bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(30, bounds.Height);
```

### Guarda anche

* class [NodeRendererBase](../)
* spazio dei nomi [Aspose.Words.Rendering](../../noderendererbase/)
* assemblea [Aspose.Words](../../../)

---

## GetSizeInPixels(float, float, float) {#getsizeinpixels_1}

Calcola la dimensione della forma in pixel per un fattore di zoom e una risoluzione specificati.

```csharp
public Size GetSizeInPixels(float scale, float horizontalDpi, float verticalDpi)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| scale | Single | Il fattore di zoom (1,0 è 100%). |
| horizontalDpi | Single | La risoluzione orizzontale da convertire da punti a pixel (punti per pollice). |
| verticalDpi | Single | La risoluzione verticale da convertire da punti a pixel (punti per pollice). |

### Valore di ritorno

La dimensione della forma in pixel.

### Osservazioni

Questo metodo converte[`SizeInPoints`](../sizeinpoints/) nella dimensione in pixel ed è utile quando vuoi creare una bitmap per rendere ordinatamente la forma sulla bitmap.

### Esempi

Mostra come misurare e ridimensionare le forme.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);
OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

// Verifica la dimensione dell'immagine che l'oggetto OfficeMath creerà quando ne eseguiremo il rendering.
Assert.AreEqual(119.0f, renderer.SizeInPoints.Width, 0.2f);
Assert.AreEqual(13.0f, renderer.SizeInPoints.Height, 0.1f);

Assert.AreEqual(119.0f, renderer.BoundsInPoints.Width, 0.2f);
Assert.AreEqual(13.0f, renderer.BoundsInPoints.Height, 0.1f);

// Le forme con parti trasparenti possono contenere valori diversi nelle proprietà "OpaqueBoundsInPoints".
Assert.AreEqual(119.0f, renderer.OpaqueBoundsInPoints.Width, 0.2f);
Assert.AreEqual(14.2f, renderer.OpaqueBoundsInPoints.Height, 0.1f);

// Ottieni la dimensione della forma in pixel, con ridimensionamento lineare a un DPI specifico.
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(18, bounds.Height);

// Ottieni la dimensione della forma in pixel, ma con un DPI diverso per le dimensioni orizzontale e verticale.
bounds = renderer.GetBoundsInPixels(1.0f, 96.0f, 150.0f);
Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(28, bounds.Height);

// Anche qui i limiti opachi possono variare.
bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(18, bounds.Height);

bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(30, bounds.Height);
```

### Guarda anche

* class [NodeRendererBase](../)
* spazio dei nomi [Aspose.Words.Rendering](../../noderendererbase/)
* assemblea [Aspose.Words](../../../)


