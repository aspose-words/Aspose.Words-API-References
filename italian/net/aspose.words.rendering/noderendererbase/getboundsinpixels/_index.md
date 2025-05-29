---
title: NodeRendererBase.GetBoundsInPixels
linktitle: GetBoundsInPixels
articleTitle: GetBoundsInPixels
second_title: Aspose.Words per .NET
description: Scopri il metodo GetBoundsInPixels di NodeRendererBase per calcolare con precisione le dimensioni delle forme in pixel in base allo zoom e alla risoluzione, per una precisione migliorata.
type: docs
weight: 40
url: /it/net/aspose.words.rendering/noderendererbase/getboundsinpixels/
---
## GetBoundsInPixels(*float, float*) {#getboundsinpixels}

Calcola i limiti della forma in pixel per un fattore di zoom e una risoluzione specificati.

```csharp
public Rectangle GetBoundsInPixels(float scale, float dpi)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| scale | Single | Fattore di zoom (1,0 è 100%). |
| dpi | Single | La risoluzione (orizzontale e verticale) per convertire da punti a pixel (punti per pollice). |

### Valore di ritorno

Il riquadro di delimitazione effettivo (come visualizzato sulla pagina) della forma in pixel.

## Osservazioni

Questo metodo converte[`BoundsInPoints`](../boundsinpoints/) in rettangolo in pixel.

## Esempi

Mostra come misurare e scalare le forme.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);
OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

// Verificare la dimensione dell'immagine che l'oggetto OfficeMath creerà quando la renderemo.
Assert.AreEqual(122.0f, renderer.SizeInPoints.Width, 0.25f);
Assert.AreEqual(13.0f, renderer.SizeInPoints.Height, 0.15f);

Assert.AreEqual(122.0f, renderer.BoundsInPoints.Width, 0.25f);
Assert.AreEqual(13.0f, renderer.BoundsInPoints.Height, 0.15f);

// Le forme con parti trasparenti possono contenere valori diversi nelle proprietà "OpaqueBoundsInPoints".
Assert.AreEqual(122.0f, renderer.OpaqueBoundsInPoints.Width, 0.25f);
Assert.AreEqual(14.2f, renderer.OpaqueBoundsInPoints.Height, 0.1f);

// Ottieni la dimensione della forma in pixel, con ridimensionamento lineare a un DPI specifico.
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(18, bounds.Height);

// Ottieni la dimensione della forma in pixel, ma con un DPI diverso per le dimensioni orizzontali e verticali.
bounds = renderer.GetBoundsInPixels(1.0f, 96.0f, 150.0f);
Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(27, bounds.Height);

// Anche qui i limiti opachi possono variare.
bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(19, bounds.Height);

bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(29, bounds.Height);
```

### Guarda anche

* class [NodeRendererBase](../)
* spazio dei nomi [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* assemblea [Aspose.Words](../../../)

---

## GetBoundsInPixels(*float, float, float*) {#getboundsinpixels_1}

Calcola i limiti della forma in pixel per un fattore di zoom e una risoluzione specificati.

```csharp
public Rectangle GetBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| scale | Single | Fattore di zoom (1,0 è 100%). |
| horizontalDpi | Single | Risoluzione orizzontale per convertire da punti a pixel (punti per pollice). |
| verticalDpi | Single | Risoluzione verticale per convertire da punti a pixel (punti per pollice). |

### Valore di ritorno

Il riquadro di delimitazione effettivo (come visualizzato sulla pagina) della forma in pixel.

## Osservazioni

Questo metodo converte[`BoundsInPoints`](../boundsinpoints/) in rettangolo in pixel.

## Esempi

Mostra come misurare e scalare le forme.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);
OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

// Verificare la dimensione dell'immagine che l'oggetto OfficeMath creerà quando la renderemo.
Assert.AreEqual(122.0f, renderer.SizeInPoints.Width, 0.25f);
Assert.AreEqual(13.0f, renderer.SizeInPoints.Height, 0.15f);

Assert.AreEqual(122.0f, renderer.BoundsInPoints.Width, 0.25f);
Assert.AreEqual(13.0f, renderer.BoundsInPoints.Height, 0.15f);

// Le forme con parti trasparenti possono contenere valori diversi nelle proprietà "OpaqueBoundsInPoints".
Assert.AreEqual(122.0f, renderer.OpaqueBoundsInPoints.Width, 0.25f);
Assert.AreEqual(14.2f, renderer.OpaqueBoundsInPoints.Height, 0.1f);

// Ottieni la dimensione della forma in pixel, con ridimensionamento lineare a un DPI specifico.
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(18, bounds.Height);

// Ottieni la dimensione della forma in pixel, ma con un DPI diverso per le dimensioni orizzontali e verticali.
bounds = renderer.GetBoundsInPixels(1.0f, 96.0f, 150.0f);
Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(27, bounds.Height);

// Anche qui i limiti opachi possono variare.
bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(19, bounds.Height);

bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(29, bounds.Height);
```

### Guarda anche

* class [NodeRendererBase](../)
* spazio dei nomi [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* assemblea [Aspose.Words](../../../)
