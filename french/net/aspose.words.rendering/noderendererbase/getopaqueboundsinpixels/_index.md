---
title: NodeRendererBase.GetOpaqueBoundsInPixels
linktitle: GetOpaqueBoundsInPixels
articleTitle: GetOpaqueBoundsInPixels
second_title: Aspose.Words pour .NET
description: Découvrez comment la méthode NodeRendererBase GetOpaqueBoundsInPixels calcule efficacement les limites de forme en pixels, en optimisant le zoom et la résolution.
type: docs
weight: 50
url: /fr/net/aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/
---
## GetOpaqueBoundsInPixels(*float, float*) {#getopaqueboundsinpixels}

Calcule les limites opaques de la forme en pixels pour un facteur de zoom et une résolution spécifiés.

```csharp
public Rectangle GetOpaqueBoundsInPixels(float scale, float dpi)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| scale | Single | Le facteur de zoom (1,0 est 100 %). |
| dpi | Single | La résolution pour convertir des points en pixels (points par pouce). |

### Return_Value

Le rectangle opaque de la forme en pixels.

## Remarques

Cette méthode convertit[`OpaqueBoundsInPoints`](../opaqueboundsinpoints/) en rectangle en pixels et c'est utile lorsque vous souhaitez créer une bitmap pour rendre la forme avec uniquement la partie opaque de la forme.

## Exemples

Montre comment mesurer et mettre à l'échelle des formes.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);
OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

// Vérifiez la taille de l'image que l'objet OfficeMath créera lorsque nous la rendrons.
Assert.AreEqual(122.0f, renderer.SizeInPoints.Width, 0.25f);
Assert.AreEqual(13.0f, renderer.SizeInPoints.Height, 0.15f);

Assert.AreEqual(122.0f, renderer.BoundsInPoints.Width, 0.25f);
Assert.AreEqual(13.0f, renderer.BoundsInPoints.Height, 0.15f);

// Les formes avec des parties transparentes peuvent contenir des valeurs différentes dans les propriétés « OpaqueBoundsInPoints ».
Assert.AreEqual(122.0f, renderer.OpaqueBoundsInPoints.Width, 0.25f);
Assert.AreEqual(14.2f, renderer.OpaqueBoundsInPoints.Height, 0.1f);

// Obtenez la taille de la forme en pixels, avec une mise à l'échelle linéaire vers un DPI spécifique.
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(18, bounds.Height);

// Obtenez la taille de la forme en pixels, mais avec un DPI différent pour les dimensions horizontales et verticales.
bounds = renderer.GetBoundsInPixels(1.0f, 96.0f, 150.0f);
Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(27, bounds.Height);

// Les limites opaques peuvent également varier ici.
bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(19, bounds.Height);

bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(29, bounds.Height);
```

### Voir également

* class [NodeRendererBase](../)
* espace de noms [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* Assemblée [Aspose.Words](../../../)

---

## GetOpaqueBoundsInPixels(*float, float, float*) {#getopaqueboundsinpixels_1}

Calcule les limites opaques de la forme en pixels pour un facteur de zoom et une résolution spécifiés.

```csharp
public Rectangle GetOpaqueBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| scale | Single | Le facteur de zoom (1,0 est 100 %). |
| horizontalDpi | Single | La résolution horizontale pour convertir des points en pixels (points par pouce). |
| verticalDpi | Single | La résolution verticale pour convertir des points en pixels (points par pouce). |

### Return_Value

Le rectangle opaque de la forme en pixels.

## Remarques

Cette méthode convertit[`OpaqueBoundsInPoints`](../opaqueboundsinpoints/) en rectangle en pixels et c'est utile lorsque vous souhaitez créer une bitmap pour rendre la forme avec uniquement la partie opaque de la forme.

## Exemples

Montre comment mesurer et mettre à l'échelle des formes.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);
OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

// Vérifiez la taille de l'image que l'objet OfficeMath créera lorsque nous la rendrons.
Assert.AreEqual(122.0f, renderer.SizeInPoints.Width, 0.25f);
Assert.AreEqual(13.0f, renderer.SizeInPoints.Height, 0.15f);

Assert.AreEqual(122.0f, renderer.BoundsInPoints.Width, 0.25f);
Assert.AreEqual(13.0f, renderer.BoundsInPoints.Height, 0.15f);

// Les formes avec des parties transparentes peuvent contenir des valeurs différentes dans les propriétés « OpaqueBoundsInPoints ».
Assert.AreEqual(122.0f, renderer.OpaqueBoundsInPoints.Width, 0.25f);
Assert.AreEqual(14.2f, renderer.OpaqueBoundsInPoints.Height, 0.1f);

// Obtenez la taille de la forme en pixels, avec une mise à l'échelle linéaire vers un DPI spécifique.
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(18, bounds.Height);

// Obtenez la taille de la forme en pixels, mais avec un DPI différent pour les dimensions horizontales et verticales.
bounds = renderer.GetBoundsInPixels(1.0f, 96.0f, 150.0f);
Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(27, bounds.Height);

// Les limites opaques peuvent également varier ici.
bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(19, bounds.Height);

bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(29, bounds.Height);
```

### Voir également

* class [NodeRendererBase](../)
* espace de noms [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* Assemblée [Aspose.Words](../../../)
