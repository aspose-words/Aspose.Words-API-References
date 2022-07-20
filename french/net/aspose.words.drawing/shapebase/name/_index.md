---
title: Name
second_title: Référence de l'API Aspose.Words pour .NET
description: Obtient ou définit le nom de la forme facultative.
type: docs
weight: 380
url: /fr/net/aspose.words.drawing/shapebase/name/
---
## ShapeBase.Name property

Obtient ou définit le nom de la forme facultative.

```csharp
public string Name { get; set; }
```

### Remarques

La valeur par défaut est une chaîne vide.

Ne peut pas être nul, mais peut être une chaîne vide.

### Exemples

Montre comment utiliser le texte alternatif d'une forme.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertShape(ShapeType.Cube, 150, 150);
shape.Name = "MyCube";

shape.AlternativeText = "Alt text for MyCube.";

// On peut accéder au texte alternatif d'une forme en faisant un clic droit dessus, puis via "Format AutoShape" -> "Texte alternatif".
doc.Save(ArtifactsDir + "Shape.AltText.docx");

// Enregistrez le document au format HTML, puis supprimez l'image liée qui appartient à notre forme.
// Le navigateur qui lit notre code HTML affichera le texte alternatif à la place de l'image manquante.
doc.Save(ArtifactsDir + "Shape.AltText.html");
```

### Voir également

* class [ShapeBase](../../shapebase)
* espace de noms [Aspose.Words.Drawing](../../shapebase)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->