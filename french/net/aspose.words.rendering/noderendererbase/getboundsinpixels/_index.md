---
title: GetBoundsInPixels
second_title: Référence de l'API Aspose.Words pour .NET
description: Calcule les limites de la forme en pixels pour un facteur de zoom et une résolution spécifiés.
type: docs
weight: 40
url: /fr/net/aspose.words.rendering/noderendererbase/getboundsinpixels/
---
## GetBoundsInPixels(float, float) {#getboundsinpixels}

Calcule les limites de la forme en pixels pour un facteur de zoom et une résolution spécifiés.

```csharp
public Rectangle GetBoundsInPixels(float scale, float dpi)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| scale | Single | Le facteur de zoom (1,0 correspond à 100 %). |
| dpi | Single | La résolution (horizontale et verticale) pour convertir des points en pixels (points par pouce). |

### Return_Value

Le cadre de délimitation réel (tel que rendu sur la page) de la forme en pixels.

### Remarques

Cette méthode convertit[`BoundsInPoints`](../boundsinpoints) en rectangle en pixels.

### Exemples

Montre comment mesurer et mettre à l'échelle des formes.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);
OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

// Vérifiez la taille de l'image que l'objet OfficeMath créera lors du rendu.
Assert.AreEqual(119.0f, renderer.SizeInPoints.Width, 0.2f);
Assert.AreEqual(13.0f, renderer.SizeInPoints.Height, 0.1f);

Assert.AreEqual(119.0f, renderer.BoundsInPoints.Width, 0.2f);
Assert.AreEqual(13.0f, renderer.BoundsInPoints.Height, 0.1f);

// Les formes avec des parties transparentes peuvent contenir des valeurs différentes dans les propriétés "OpaqueBoundsInPoints".
Assert.AreEqual(119.0f, renderer.OpaqueBoundsInPoints.Width, 0.2f);
Assert.AreEqual(14.2f, renderer.OpaqueBoundsInPoints.Height, 0.1f);

// Obtient la taille de la forme en pixels, avec une mise à l'échelle linéaire à un DPI spécifique.
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(18, bounds.Height);

// Obtient la taille de la forme en pixels, mais avec un DPI différent pour les dimensions horizontales et verticales.
bounds = renderer.GetBoundsInPixels(1.0f, 96.0f, 150.0f);
Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(28, bounds.Height);

// Les limites opaques peuvent également varier ici.
bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(18, bounds.Height);

bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(30, bounds.Height);
```

### Voir également

* class [NodeRendererBase](../../noderendererbase)
* espace de noms [Aspose.Words.Rendering](../../noderendererbase)
* Assemblée [Aspose.Words](../../../)

---

## GetBoundsInPixels(float, float, float) {#getboundsinpixels_1}

Calcule les limites de la forme en pixels pour un facteur de zoom et une résolution spécifiés.

```csharp
public Rectangle GetBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| scale | Single | Le facteur de zoom (1,0 correspond à 100 %). |
| horizontalDpi | Single | La résolution horizontale pour convertir des points en pixels (points par pouce). |
| verticalDpi | Single | La résolution verticale pour convertir des points en pixels (points par pouce). |

### Return_Value

Le cadre de délimitation réel (tel que rendu sur la page) de la forme en pixels.

### Remarques

Cette méthode convertit[`BoundsInPoints`](../boundsinpoints) en rectangle en pixels.

### Exemples

Montre comment mesurer et mettre à l'échelle des formes.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);
OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

// Vérifiez la taille de l'image que l'objet OfficeMath créera lors du rendu.
Assert.AreEqual(119.0f, renderer.SizeInPoints.Width, 0.2f);
Assert.AreEqual(13.0f, renderer.SizeInPoints.Height, 0.1f);

Assert.AreEqual(119.0f, renderer.BoundsInPoints.Width, 0.2f);
Assert.AreEqual(13.0f, renderer.BoundsInPoints.Height, 0.1f);

// Les formes avec des parties transparentes peuvent contenir des valeurs différentes dans les propriétés "OpaqueBoundsInPoints".
Assert.AreEqual(119.0f, renderer.OpaqueBoundsInPoints.Width, 0.2f);
Assert.AreEqual(14.2f, renderer.OpaqueBoundsInPoints.Height, 0.1f);

// Obtient la taille de la forme en pixels, avec une mise à l'échelle linéaire à un DPI spécifique.
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(18, bounds.Height);

// Obtient la taille de la forme en pixels, mais avec un DPI différent pour les dimensions horizontales et verticales.
bounds = renderer.GetBoundsInPixels(1.0f, 96.0f, 150.0f);
Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(28, bounds.Height);

// Les limites opaques peuvent également varier ici.
bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(18, bounds.Height);

bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(30, bounds.Height);
```

### Voir également

* class [NodeRendererBase](../../noderendererbase)
* espace de noms [Aspose.Words.Rendering](../../noderendererbase)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
