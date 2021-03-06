---
title: ScreenTip
second_title: Référence de l'API Aspose.Words pour .NET
description: Définit le texte affiché lorsque le pointeur de la souris se déplace sur la forme.
type: docs
weight: 440
url: /fr/net/aspose.words.drawing/shapebase/screentip/
---
## ShapeBase.ScreenTip property

Définit le texte affiché lorsque le pointeur de la souris se déplace sur la forme.

```csharp
public string ScreenTip { get; set; }
```

### Remarques

La valeur par défaut est une chaîne vide.

### Exemples

Montre comment insérer une forme qui contient une image et qui est également un lien hypertexte.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.HRef = "https://forum.aspose.com/" ;
shape.Target = "New Window";
shape.ScreenTip = "Aspose.Words Support Forums";

// Ctrl + clic gauche sur la forme dans Microsoft Word ouvrira une nouvelle fenêtre de navigateur Web
// et nous amène au lien hypertexte dans la propriété "HRef".
doc.Save(ArtifactsDir + "Image.InsertImageWithHyperlink.docx");
```

### Voir également

* class [ShapeBase](../../shapebase)
* espace de noms [Aspose.Words.Drawing](../../shapebase)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
