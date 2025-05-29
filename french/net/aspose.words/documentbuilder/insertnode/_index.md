---
title: DocumentBuilder.InsertNode
linktitle: InsertNode
articleTitle: InsertNode
second_title: Aspose.Words pour .NET
description: Améliorez la création de vos documents grâce à la méthode InsertNode de DocumentBuilder. Insérez facilement des nœuds avant le curseur pour une édition fluide !
type: docs
weight: 410
url: /fr/net/aspose.words/documentbuilder/insertnode/
---
## DocumentBuilder.InsertNode method

Insère un nœud avant le curseur.

```csharp
public void InsertNode(Node node)
```

## Exemples

Montre comment insérer une image liée dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFileName = ImageDir + "Windows MetaFile.wmf";

// Vous trouverez ci-dessous deux manières d'appliquer une image à une forme afin qu'elle puisse l'afficher.
// 1 - Définissez la forme pour contenir l'image.
Shape shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SetImage(imageFileName);

builder.InsertNode(shape);

doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx");

// Chaque image que nous stockons dans shape augmentera la taille de notre document.
Assert.True(70000 < new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx").Length);

doc.FirstSection.Body.FirstParagraph.RemoveAllChildren();

// 2 - Définissez la forme pour qu'elle soit liée à un fichier image dans le système de fichiers local.
shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SourceFullName = imageFileName;

builder.InsertNode(shape);
doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx");

// Lier des images permettra d'économiser de l'espace et d'obtenir un document plus petit.
// Cependant, le document ne peut afficher correctement l'image que pendant
// le fichier image est présent à l'emplacement vers lequel pointe la propriété « SourceFullName » de la forme.
Assert.True(10000 > new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx").Length);
```

### Voir également

* class [Node](../../node/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
