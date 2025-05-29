---
title: ShapeBase.Target
linktitle: Target
articleTitle: Target
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ShapeBase Target pour définir ou récupérer facilement des cadres cibles d'hyperlien pour vos formes, améliorant ainsi la navigation et l'expérience de l'utilisateur.
type: docs
weight: 560
url: /fr/net/aspose.words.drawing/shapebase/target/
---
## ShapeBase.Target property

Obtient ou définit le cadre cible pour le lien hypertexte de forme.

```csharp
public string Target { get; set; }
```

## Remarques

La valeur par défaut est une chaîne vide.

## Exemples

Montre comment insérer une forme qui contient une image et qui est également un hyperlien.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.HRef = "https://forum.aspose.com/";
shape.Target = "New Window";
shape.ScreenTip = "Aspose.Words Support Forums";

// Ctrl + clic gauche sur la forme dans Microsoft Word ouvrira une nouvelle fenêtre de navigateur Web
// et nous amène à l'hyperlien dans la propriété "HRef".
doc.Save(ArtifactsDir + "Image.InsertImageWithHyperlink.docx");
```

### Voir également

* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
