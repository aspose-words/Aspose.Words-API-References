---
title: Shape
linktitle: Shape
articleTitle: Shape
second_title: Aspose.Words pour .NET
description: Créez des formes uniques en toute simplicité grâce à notre Constructeur de formes. Concevez des formes personnalisées et améliorez vos projets avec facilité et précision !
type: docs
weight: 10
url: /fr/net/aspose.words.drawing/shape/shape/
---
## Shape constructor

Crée un nouvel objet de forme.

```csharp
public Shape(DocumentBase doc, ShapeType shapeType)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| doc | DocumentBase | Le document du propriétaire. |
| shapeType | ShapeType | Le type de forme à créer. |

## Remarques

Vous devez spécifier les propriétés de forme souhaitées après avoir créé une forme.

## Exemples

Montre comment insérer une forme avec une image du système de fichiers local dans un document.

```csharp
Document doc = new Document();

// Le constructeur public de la classe « Shape » créera une forme avec le type de balisage « ShapeMarkupLanguage.Vml ».
// Si vous devez créer une forme d'un type non primitif, tel que SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// Coins supérieurs un arrondi un coupé, Coin unique arrondi, Coins supérieurs arrondis ou Coins diagonaux arrondis,
// veuillez utiliser DocumentBuilder.InsertShape.
Shape shape = new Shape(doc, ShapeType.Image);
shape.ImageData.SetImage(ImageDir + "Windows MetaFile.wmf");
shape.Width = 100;
shape.Height = 100;

doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

doc.Save(ArtifactsDir + "Image.FromFile.docx");
```

Montre comment créer et formater une zone de texte.

```csharp
Document doc = new Document();

// Créer une zone de texte flottante.
Shape textBox = new Shape(doc, ShapeType.TextBox);
textBox.WrapType = WrapType.None;
textBox.Height = 50;
textBox.Width = 200;

// Définissez l'alignement horizontal et vertical du texte à l'intérieur de la forme.
textBox.HorizontalAlignment = HorizontalAlignment.Center;
textBox.VerticalAlignment = VerticalAlignment.Top;

// Ajoutez un paragraphe à la zone de texte et ajoutez une séquence de texte que la zone de texte affichera.
textBox.AppendChild(new Paragraph(doc));
Paragraph para = textBox.FirstParagraph;
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;
Run run = new Run(doc);
run.Text = "Hello world!";
para.AppendChild(run);

doc.FirstSection.Body.FirstParagraph.AppendChild(textBox);

doc.Save(ArtifactsDir + "Shape.CreateTextBox.docx");
```

### Voir également

* class [DocumentBase](../../../aspose.words/documentbase/)
* enum [ShapeType](../../shapetype/)
* class [Shape](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
