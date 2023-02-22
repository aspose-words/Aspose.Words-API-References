---
title: ShapeBase.Title
second_title: Référence de l'API Aspose.Words pour .NET
description: ShapeBase propriété. Obtient ou définit le titre légende de lobjet forme actuel.
type: docs
weight: 490
url: /fr/net/aspose.words.drawing/shapebase/title/
---
## ShapeBase.Title property

Obtient ou définit le titre (légende) de l'objet forme actuel.

```csharp
public string Title { get; set; }
```

### Remarques

La valeur par défaut est une chaîne vide.

Ne peut pas être nul, mais peut être une chaîne vide.

### Exemples

Montre comment définir le titre d'une forme.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crée une forme, lui donne un titre, puis l'ajoute au document.
Shape shape = new Shape(doc, ShapeType.Cube);
shape.Width = 200;
shape.Height = 200;
shape.Title = "My cube";

builder.InsertNode(shape);

// Lorsque nous enregistrons un document avec une forme qui a un titre,
// Aspose.Words stockera ce titre dans le texte alternatif de la forme.
doc.Save(ArtifactsDir + "Shape.Title.docx");

doc = new Document(ArtifactsDir + "Shape.Title.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual(string.Empty, shape.Title);
Assert.AreEqual("Title: My cube", shape.AlternativeText);
```

### Voir également

* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../shapebase/)
* Assemblée [Aspose.Words](../../../)


