---
title: ShapeBase.ScreenTip
linktitle: ScreenTip
articleTitle: ScreenTip
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ShapeBase ScreenTip, améliorez l'expérience utilisateur en personnalisant le texte de l'info-bulle qui apparaît au survol de la souris sur les formes.
type: docs
weight: 510
url: /fr/net/aspose.words.drawing/shapebase/screentip/
---
## ShapeBase.ScreenTip property

Définit le texte affiché lorsque le pointeur de la souris se déplace sur la forme.

```csharp
public string ScreenTip { get; set; }
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
