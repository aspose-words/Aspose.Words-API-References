---
title: TextBox.NoTextRotation
linktitle: NoTextRotation
articleTitle: NoTextRotation
second_title: Aspose.Words pour .NET
description: TextBox NoTextRotation propriété. Obtient ou définit une valeur booléenne indiquant que le texte de TextBox ne doit pas pivoter lorsque la forme est pivotée en C#.
type: docs
weight: 80
url: /fr/net/aspose.words.drawing/textbox/notextrotation/
---
## TextBox.NoTextRotation property

Obtient ou définit une valeur booléenne indiquant que le texte de TextBox ne doit pas pivoter lorsque la forme est pivotée.

```csharp
public bool NoTextRotation { get; set; }
```

## Remarques

La valeur par défaut est`FAUX`

## Exemples

Montre comment désactiver la rotation du texte lorsque la forme pivote.

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
