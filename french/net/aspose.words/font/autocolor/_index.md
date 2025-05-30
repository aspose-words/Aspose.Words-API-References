---
title: Font.AutoColor
linktitle: AutoColor
articleTitle: AutoColor
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Font AutoColor  obtenez la couleur actuelle du texte (noir ou blanc) pour des ajustements automatiques. Optimisez votre design sans effort !
type: docs
weight: 20
url: /fr/net/aspose.words/font/autocolor/
---
## Font.AutoColor property

Renvoie la couleur calculée actuelle du texte (noir ou blanc) à utiliser pour la « couleur automatique ». Si la couleur n'est pas « auto », renvoie[`Color`](../color/) .

```csharp
public Color AutoColor { get; }
```

## Remarques

Lorsque le texte est défini sur « couleur automatique », sa couleur réelle est calculée automatiquement afin qu'il soit lisible par rapport à la couleur d'arrière-plan. Lorsque vous modifiez la couleur d'arrière-plan, la couleur du texte passe automatiquement au noir ou au blanc dans MS Word pour une lisibilité optimale.

## Exemples

Montre comment améliorer la lisibilité en sélectionnant automatiquement la couleur du texte en fonction de la luminosité de son arrière-plan.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Si l'objet Font d'une exécution ne spécifie pas la couleur du texte, il le sera automatiquement
// sélectionnez soit le noir, soit le blanc en fonction de la couleur d'arrière-plan.
Assert.AreEqual(Color.Empty.ToArgb(), builder.Font.Color.ToArgb());

// La couleur par défaut du texte est le noir. Si la couleur d'arrière-plan est sombre, le texte noir sera difficile à lire.
// Pour résoudre ce problème, la propriété AutoColor affichera ce texte en blanc.
builder.Font.Shading.BackgroundPatternColor = Color.DarkBlue;

builder.Writeln("The text color automatically chosen for this run is white.");

Assert.AreEqual(Color.White.ToArgb(), doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.AutoColor.ToArgb());

// Si nous changeons l'arrière-plan en une couleur claire, le noir sera une couleur plus
// couleur de texte plus appropriée que le blanc pour que la couleur automatique l'affiche en noir.
builder.Font.Shading.BackgroundPatternColor = Color.LightBlue;

builder.Writeln("The text color automatically chosen for this run is black.");

Assert.AreEqual(Color.Black.ToArgb(), doc.FirstSection.Body.Paragraphs[1].Runs[0].Font.AutoColor.ToArgb());

doc.Save(ArtifactsDir + "Font.SetFontAutoColor.docx");
```

### Voir également

* class [Font](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
