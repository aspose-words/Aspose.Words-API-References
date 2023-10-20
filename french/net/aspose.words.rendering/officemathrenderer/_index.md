---
title: OfficeMathRenderer Class
linktitle: OfficeMathRenderer
articleTitle: OfficeMathRenderer
second_title: Aspose.Words pour .NET
description: Aspose.Words.Rendering.OfficeMathRenderer classe. Fournit des méthodes pour restituer un individuOfficeMath vers une image raster ou vectorielle ou vers un objet graphique en C#.
type: docs
weight: 4560
url: /fr/net/aspose.words.rendering/officemathrenderer/
---
## OfficeMathRenderer class

Fournit des méthodes pour restituer un individu[`OfficeMath`](../../aspose.words.math/officemath/) vers une image raster ou vectorielle ou vers un objet graphique.

Pour en savoir plus, visitez le[Travailler avec OfficeMath](https://docs.aspose.com/words/net/working-with-officemath/) article documentaire.

```csharp
public class OfficeMathRenderer : NodeRendererBase
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [OfficeMathRenderer](officemathrenderer/)(*[OfficeMath](../../aspose.words.math/officemath/)*) | Initialise une nouvelle instance de cette classe. |

## Propriétés

| Nom | La description |
| --- | --- |
| [BoundsInPoints](../../aspose.words.rendering/noderendererbase/boundsinpoints/) { get; } | Obtient les limites réelles de la forme en points. |
| [OpaqueBoundsInPoints](../../aspose.words.rendering/noderendererbase/opaqueboundsinpoints/) { get; } | Obtient les limites opaques de la forme en points. |
| [SizeInPoints](../../aspose.words.rendering/noderendererbase/sizeinpoints/) { get; } | Obtient la taille réelle de la forme en points. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels/)(*float, float*) | Calcule les limites de la forme en pixels pour un facteur de zoom et une résolution spécifiés. |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels/)(*float, float, float*) | Calcule les limites de la forme en pixels pour un facteur de zoom et une résolution spécifiés. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/)(*float, float*) | Calcule les limites opaques de la forme en pixels pour un facteur de zoom et une résolution spécifiés. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/)(*float, float, float*) | Calcule les limites opaques de la forme en pixels pour un facteur de zoom et une résolution spécifiés. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels/)(*float, float*) | Calcule la taille de la forme en pixels pour un facteur de zoom et une résolution spécifiés. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels/)(*float, float, float*) | Calcule la taille de la forme en pixels pour un facteur de zoom et une résolution spécifiés. |
| [RenderToScale](../../aspose.words.rendering/noderendererbase/rendertoscale/)(*Graphics, float, float, float*) | Rend la forme dans unGraphics objet à une échelle spécifiée. |
| [RenderToSize](../../aspose.words.rendering/noderendererbase/rendertosize/)(*Graphics, float, float, float, float*) | Rend la forme dans unGraphics objet à une taille spécifiée. |
| [Save](../../aspose.words.rendering/noderendererbase/save/)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Rend la forme dans une image et l'enregistre dans un flux. |
| [Save](../../aspose.words.rendering/noderendererbase/save/)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Rend la forme dans une image et l'enregistre dans un fichier. |

## Exemples

Montre comment mesurer et mettre à l’échelle des formes.

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

// Obtenez la taille de la forme en pixels, avec une mise à l'échelle linéaire vers un DPI spécifique.
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(18, bounds.Height);

// Récupère la taille de la forme en pixels, mais avec un DPI différent pour les dimensions horizontales et verticales.
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

* class [NodeRendererBase](../noderendererbase/)
* espace de noms [Aspose.Words.Rendering](../../aspose.words.rendering/)
* Assemblée [Aspose.Words](../../)
