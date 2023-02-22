---
title: OfficeMathRenderer.OfficeMathRenderer
second_title: Référence de l'API Aspose.Words pour .NET
description: OfficeMathRenderer constructeur. Initialise une nouvelle instance de cette classe.
type: docs
weight: 10
url: /fr/net/aspose.words.rendering/officemathrenderer/officemathrenderer/
---
## OfficeMathRenderer constructor

Initialise une nouvelle instance de cette classe.

```csharp
public OfficeMathRenderer(OfficeMath math)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| math | OfficeMath | L'objet OfficeMath que vous souhaitez afficher. |

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

* class [OfficeMath](../../../aspose.words.math/officemath/)
* class [OfficeMathRenderer](../)
* espace de noms [Aspose.Words.Rendering](../../officemathrenderer/)
* Assemblée [Aspose.Words](../../../)


