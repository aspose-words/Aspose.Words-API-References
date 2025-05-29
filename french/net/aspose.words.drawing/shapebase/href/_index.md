---
title: ShapeBase.HRef
linktitle: HRef
articleTitle: HRef
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ShapeBase HRef pour gérer facilement les adresses d'hyperliens complètes pour vos formes, améliorant ainsi l'interactivité et la fonctionnalité de votre conception.
type: docs
weight: 250
url: /fr/net/aspose.words.drawing/shapebase/href/
---
## ShapeBase.HRef property

Obtient ou définit l'adresse complète du lien hypertexte pour une forme.

```csharp
public string HRef { get; set; }
```

## Remarques

La valeur par défaut est une chaîne vide.

Vous trouverez ci-dessous des exemples de valeurs valides pour cette propriété :

URI complet :`https://www.aspose.com/`.

Nom complet du fichier :`C:\\Mes documents\\SalesReport.doc`.

URI relatif :`../../../resource.txt`

Nom de fichier relatif :`..\\Mes documents\\SalesReport.doc`.

Marquer dans un autre document :`https://www.aspose.com/Products/Default.aspx#Suites`

Marquer dans ce document :`#BookmakName`.

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
