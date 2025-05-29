---
title: OfficeMath.GetMathRenderer
linktitle: GetMathRenderer
articleTitle: GetMathRenderer
second_title: Aspose.Words pour .NET
description: Découvrez la méthode GetMathRenderer d'OfficeMath pour convertir sans effort des équations en images, améliorant ainsi vos documents avec des visuels clairs et professionnels.
type: docs
weight: 90
url: /fr/net/aspose.words.math/officemath/getmathrenderer/
---
## OfficeMath.GetMathRenderer method

Crée et renvoie un objet qui peut être utilisé pour rendre cette équation dans une image.

```csharp
public OfficeMathRenderer GetMathRenderer()
```

### Return_Value

L'objet de rendu pour cette équation.

## Remarques

Cette méthode invoque simplement le[`OfficeMathRenderer`](../../../aspose.words.rendering/officemathrenderer/) constructeur et passe cet objet en paramètre.

## Exemples

Montre comment restituer un objet Office Math dans un fichier image dans le système de fichiers local.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// Créez un objet « ImageSaveOptions » à transmettre à la méthode « Save » du moteur de rendu du nœud pour modifier
// comment il rend le nœud OfficeMath dans une image.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// Définissez la propriété « Scale » sur 5 pour rendre l'objet à cinq fois sa taille d'origine.
saveOptions.Scale = 5;

math.GetMathRenderer().Save(ArtifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

### Voir également

* class [OfficeMathRenderer](../../../aspose.words.rendering/officemathrenderer/)
* class [OfficeMath](../)
* espace de noms [Aspose.Words.Math](../../../aspose.words.math/)
* Assemblée [Aspose.Words](../../../)
