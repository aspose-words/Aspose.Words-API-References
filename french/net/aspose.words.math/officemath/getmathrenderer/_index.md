---
title: OfficeMath.GetMathRenderer
second_title: Référence de l'API Aspose.Words pour .NET
description: OfficeMath méthode. Crée et renvoie un objet qui peut être utilisé pour restituer cette équation dans une image.
type: docs
weight: 90
url: /fr/net/aspose.words.math/officemath/getmathrenderer/
---
## OfficeMath.GetMathRenderer method

Crée et renvoie un objet qui peut être utilisé pour restituer cette équation dans une image.

```csharp
public OfficeMathRenderer GetMathRenderer()
```

### Return_Value

L'objet de rendu pour cette équation.

### Remarques

Cette méthode invoque simplement le[`OfficeMathRenderer`](../../../aspose.words.rendering/officemathrenderer/) constructeur et passe cet objet en paramètre.

### Exemples

Montre comment restituer un objet Office Math dans un fichier image dans le système de fichiers local.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// Créez un objet "ImageSaveOptions" à passer à la méthode "Save" du moteur de rendu de nœud pour modifier
// comment il restitue le nœud OfficeMath en image.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// Définissez la propriété "Scale" sur 5 pour rendre l'objet à cinq fois sa taille d'origine.
saveOptions.Scale = 5;

math.GetMathRenderer().Save(ArtifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

### Voir également

* class [OfficeMathRenderer](../../../aspose.words.rendering/officemathrenderer/)
* class [OfficeMath](../)
* espace de noms [Aspose.Words.Math](../../officemath/)
* Assemblée [Aspose.Words](../../../)


