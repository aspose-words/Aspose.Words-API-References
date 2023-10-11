---
title: ShapeBase.Target
second_title: Référence de l'API Aspose.Words pour .NET
description: ShapeBase propriété. Obtient ou définit le cadre cible pour le lien hypertexte de forme.
type: docs
weight: 520
url: /fr/net/aspose.words.drawing/shapebase/target/
---
## ShapeBase.Target property

Obtient ou définit le cadre cible pour le lien hypertexte de forme.

```csharp
public string Target { get; set; }
```

### Remarques

La valeur par défaut est une chaîne vide.

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


