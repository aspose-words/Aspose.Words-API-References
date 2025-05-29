---
title: TextBox.NoTextRotation
linktitle: NoTextRotation
articleTitle: NoTextRotation
second_title: Aspose.Words pour .NET
description: Contrôlez la rotation du texte dans votre zone de texte avec la propriété NoTextRotation. Assurez-vous que le texte est clair et lisible, même lorsque les formes sont pivotées. Améliorez votre design !
type: docs
weight: 80
url: /fr/net/aspose.words.drawing/textbox/notextrotation/
---
## TextBox.NoTextRotation property

Obtient ou définit une valeur booléenne indiquant que le texte de la zone de texte ne doit pas pivoter lorsque la forme est pivotée.

```csharp
public bool NoTextRotation { get; set; }
```

## Remarques

La valeur par défaut est`FAUX`

## Exemples

Montre comment désactiver la rotation du texte lorsque la forme est tournée.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Ellipse, 20, 20);
shape.TextBox.NoTextRotation = true;

doc.Save(ArtifactsDir + "Shape.NoTextRotation.docx");
```

### Voir également

* class [TextBox](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
