---
title: NodeRendererBase.GetOpaqueBoundsInPixels
linktitle: GetOpaqueBoundsInPixels
articleTitle: GetOpaqueBoundsInPixels
second_title: Aspose.Words per .NET
description: Scopri come il metodo GetOpaqueBoundsInPixels di NodeRendererBase calcola in modo efficiente i limiti delle forme in pixel, ottimizzandoli per zoom e risoluzione.
type: docs
weight: 50
url: /it/net/aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/
---
## GetOpaqueBoundsInPixels(*float, float*) {#getopaqueboundsinpixels}

Calcola i limiti opachi della forma in pixel per un fattore di zoom e una risoluzione specificati.

```csharp
public Rectangle GetOpaqueBoundsInPixels(float scale, float dpi)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| scale | Single | Fattore di zoom (1,0 è 100%). |
| dpi | Single | La risoluzione per convertire da punti a pixel (punti per pollice). |

### Valore di ritorno

Il rettangolo opaco della forma in pixel.

## Osservazioni

Questo metodo converte[`OpaqueBoundsInPoints`](../opaqueboundsinpoints/) in rettangolo in pixel ed è utile quando si desidera creare una bitmap per il rendering della forma con solo la parte opaca della forma.

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

## GetOpaqueBoundsInPixels(*float, float, float*) {#getopaqueboundsinpixels_1}

Calcola i limiti opachi della forma in pixel per un fattore di zoom e una risoluzione specificati.

```csharp
public Rectangle GetOpaqueBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| scale | Single | Fattore di zoom (1,0 è 100%). |
| horizontalDpi | Single | Risoluzione orizzontale per convertire da punti a pixel (punti per pollice). |
| verticalDpi | Single | Risoluzione verticale per convertire da punti a pixel (punti per pollice). |

### Valore di ritorno

Il rettangolo opaco della forma in pixel.

## Osservazioni

Questo metodo converte[`OpaqueBoundsInPoints`](../opaqueboundsinpoints/) in rettangolo in pixel ed è utile quando si desidera creare una bitmap per il rendering della forma con solo la parte opaca della forma.

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
