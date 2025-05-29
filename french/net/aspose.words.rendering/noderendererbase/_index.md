---
title: NodeRendererBase Class
linktitle: NodeRendererBase
articleTitle: NodeRendererBase
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Rendering.NodeRendererBase, votre base pour un rendu Shape et OfficeMath efficace dans le traitement des documents.
type: docs
weight: 5280
url: /fr/net/aspose.words.rendering/noderendererbase/
---
## NodeRendererBase class

Classe de base pour[`ShapeRenderer`](../shaperenderer/) et[`OfficeMathRenderer`](../officemathrenderer/) .

Pour en savoir plus, visitez le[Travailler avec des formes](https://docs.aspose.com/words/net/working-with-shapes/) article de documentation.

```csharp
public abstract class NodeRendererBase
```

## Propriétés

| Nom | La description |
| --- | --- |
| [BoundsInPoints](../../aspose.words.rendering/noderendererbase/boundsinpoints/) { get; } | Obtient les limites réelles de la forme en points. |
| [OpaqueBoundsInPoints](../../aspose.words.rendering/noderendererbase/opaqueboundsinpoints/) { get; } | Obtient les limites opaques de la forme en points. |
| [SizeInPoints](../../aspose.words.rendering/noderendererbase/sizeinpoints/) { get; } | Obtient la taille réelle de la forme en points. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels/#getboundsinpixels)(*float, float*) | Calcule les limites de la forme en pixels pour un facteur de zoom et une résolution spécifiés. |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels/#getboundsinpixels_1)(*float, float, float*) | Calcule les limites de la forme en pixels pour un facteur de zoom et une résolution spécifiés. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/#getopaqueboundsinpixels)(*float, float*) | Calcule les limites opaques de la forme en pixels pour un facteur de zoom et une résolution spécifiés. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/#getopaqueboundsinpixels_1)(*float, float, float*) | Calcule les limites opaques de la forme en pixels pour un facteur de zoom et une résolution spécifiés. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels/#getsizeinpixels)(*float, float*) | Calcule la taille de la forme en pixels pour un facteur de zoom et une résolution spécifiés. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels/#getsizeinpixels_1)(*float, float, float*) | Calcule la taille de la forme en pixels pour un facteur de zoom et une résolution spécifiés. |
| [RenderToScale](../../aspose.words.rendering/noderendererbase/rendertoscale/)(*Graphics, float, float, float*) | Rend la forme dans unGraphics objet à une échelle spécifiée. |
| [RenderToSize](../../aspose.words.rendering/noderendererbase/rendertosize/)(*Graphics, float, float, float, float*) | Rend la forme dans unGraphics objet à une taille spécifiée. |
| [Save](../../aspose.words.rendering/noderendererbase/save/#save)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Rend la forme dans une image et l'enregistre dans un flux. |
| [Save](../../aspose.words.rendering/noderendererbase/save/#save_1)(*Stream, [SvgSaveOptions](../../aspose.words.saving/svgsaveoptions/)*) | Rend la forme dans une image SVG et l'enregistre dans un flux. |
| [Save](../../aspose.words.rendering/noderendererbase/save/#save_2)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Rend la forme dans une image et l'enregistre dans un fichier. |
| [Save](../../aspose.words.rendering/noderendererbase/save/#save_3)(*string, [SvgSaveOptions](../../aspose.words.saving/svgsaveoptions/)*) | Rend la forme dans une image SVG et l'enregistre dans un fichier. |

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

* espace de noms [Aspose.Words.Rendering](../../aspose.words.rendering/)
* Assemblée [Aspose.Words](../../)
