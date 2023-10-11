---
title: ShapeBase.HRef
second_title: Référence de l'API Aspose.Words pour .NET
description: ShapeBase propriété. Obtient ou définit ladresse complète du lien hypertexte pour une forme.
type: docs
weight: 230
url: /fr/net/aspose.words.drawing/shapebase/href/
---
## ShapeBase.HRef property

Obtient ou définit l'adresse complète du lien hypertexte pour une forme.

```csharp
public string HRef { get; set; }
```

### Remarques

La valeur par défaut est une chaîne vide.

Vous trouverez ci-dessous des exemples de valeurs valides pour cette propriété :

URI complet :`https://www.aspose.com/`.

Nom complet du fichier :`C:\\Mes documents\\SalesReport.doc`.

URI relatif :`../../../resource.txt`

Nom de fichier relatif :`..\\Mes documents\\SalesReport.doc`.

Ajouter aux favoris dans un autre document :`https://www.aspose.com/Products/Default.aspx#Suites`

Ajouter à vos favoris ce document :`#BookmakName`.

### Exemples

Montre comment insérer une forme contenant une image et qui constitue également un lien hypertexte.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.HRef = "https://forum.aspose.com/";
shape.Target = "New Window";
shape.ScreenTip = "Aspose.Words Support Forums";

// Ctrl + clic gauche sur la forme dans Microsoft Word ouvrira une nouvelle fenêtre de navigateur Web
// et nous amène au lien hypertexte dans la propriété "HRef".
doc.Save(ArtifactsDir + "Image.InsertImageWithHyperlink.docx");
```

### Voir également

* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../shapebase/)
* Assemblée [Aspose.Words](../../../)


