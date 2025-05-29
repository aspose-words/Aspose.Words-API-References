---
title: TextBox Class
linktitle: TextBox
articleTitle: TextBox
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Drawing.TextBox pour personnaliser facilement l'affichage du texte dans les formes, améliorant ainsi l'attrait visuel et la fonctionnalité de votre document.
type: docs
weight: 1730
url: /fr/net/aspose.words.drawing/textbox/
---
## TextBox class

Définit les attributs qui spécifient comment un texte est affiché à l'intérieur d'une forme.

Pour en savoir plus, visitez le[Travailler avec des formes](https://docs.aspose.com/words/net/working-with-shapes/) article de documentation.

```csharp
public class TextBox
```

## Propriétés

| Nom | La description |
| --- | --- |
| [FitShapeToText](../../aspose.words.drawing/textbox/fitshapetotext/) { get; set; } | Détermine si Microsoft Word doit agrandir la forme pour l'adapter au texte. |
| [InternalMarginBottom](../../aspose.words.drawing/textbox/internalmarginbottom/) { get; set; } | Spécifie la marge inférieure intérieure en points pour une forme. |
| [InternalMarginLeft](../../aspose.words.drawing/textbox/internalmarginleft/) { get; set; } | Spécifie la marge intérieure gauche en points pour une forme. |
| [InternalMarginRight](../../aspose.words.drawing/textbox/internalmarginright/) { get; set; } | Spécifie la marge intérieure droite en points pour une forme. |
| [InternalMarginTop](../../aspose.words.drawing/textbox/internalmargintop/) { get; set; } | Spécifie la marge supérieure intérieure en points pour une forme. |
| [LayoutFlow](../../aspose.words.drawing/textbox/layoutflow/) { get; set; } | Détermine le flux de la disposition du texte dans une forme. |
| [Next](../../aspose.words.drawing/textbox/next/) { get; set; } | Renvoie ou définit un`TextBox` qui représente le prochain`TextBox`dans une séquence de formes. |
| [NoTextRotation](../../aspose.words.drawing/textbox/notextrotation/) { get; set; } | Obtient ou définit une valeur booléenne indiquant que le texte de la zone de texte ne doit pas pivoter lorsque la forme est pivotée. |
| [Parent](../../aspose.words.drawing/textbox/parent/) { get; } | Obtient une forme parente pour le`TextBox` . |
| [Previous](../../aspose.words.drawing/textbox/previous/) { get; } | Renvoie un`TextBox` qui représente le précédent`TextBox`dans une séquence de formes. |
| [TextBoxWrapMode](../../aspose.words.drawing/textbox/textboxwrapmode/) { get; set; } | Détermine la manière dont le texte s'enroule à l'intérieur d'une forme. |
| [VerticalAnchor](../../aspose.words.drawing/textbox/verticalanchor/) { get; set; } | Spécifie l'alignement vertical du texte dans une forme. |

## Méthodes

| Nom | La description |
| --- | --- |
| [BreakForwardLink](../../aspose.words.drawing/textbox/breakforwardlink/)() | Rompt le lien vers le suivant`TextBox` . |
| [IsValidLinkTarget](../../aspose.words.drawing/textbox/isvalidlinktarget/)(*TextBox*) | Détermine si cela`TextBox` peut être lié à la cible`TextBox` . |

## Remarques

Utilisez le[`TextBox`](../shape/textbox/) propriété pour accéder aux propriétés de texte d'une forme. Vous ne créez pas d'instances de la`TextBox` classe directement.

## Exemples

Montre comment définir des marges internes pour une zone de texte.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer une autre zone de texte avec des marges spécifiques.
Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 100, 100);
TextBox textBox = textBoxShape.TextBox;
textBox.InternalMarginTop = 15;
textBox.InternalMarginBottom = 15;
textBox.InternalMarginLeft = 15;
textBox.InternalMarginRight = 15;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text placed according to textbox margins.");

doc.Save(ArtifactsDir + "Shape.TextBoxMargins.docx");
```

Montre comment définir l'orientation du texte à l'intérieur d'une zone de texte.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Déplacez le générateur de documents à l'intérieur de la zone de texte et ajoutez du texte.
builder.MoveTo(textBoxShape.LastParagraph);
builder.Writeln("Hello world!");
builder.Write("Hello again!");

// Définissez la propriété « LayoutFlow » pour définir une orientation pour le contenu du texte de cette zone de texte.
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

Montre comment redimensionner une zone de texte pour qu'elle s'adapte parfaitement à son contenu.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Appliquez ces valeurs à ces deux membres pour que la forme parente s'adapte
// étroitement autour du contenu du texte, en ignorant les dimensions que nous avons définies.
textBox.FitShapeToText = true;
textBox.TextBoxWrapMode = TextBoxWrapMode.None;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text fit tightly inside textbox.");

doc.Save(ArtifactsDir + "Shape.TextBoxFitShapeToText.docx");
```

### Voir également

* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)
