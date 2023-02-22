---
title: Class TextBox
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Drawing.TextBox classe. Définit les attributs qui spécifient comment un texte est affiché à lintérieur dune forme.
type: docs
weight: 1170
url: /fr/net/aspose.words.drawing/textbox/
---
## TextBox class

Définit les attributs qui spécifient comment un texte est affiché à l'intérieur d'une forme.

```csharp
public class TextBox
```

## Propriétés

| Nom | La description |
| --- | --- |
| [FitShapeToText](../../aspose.words.drawing/textbox/fitshapetotext/) { get; set; } | Détermine si Microsoft Word agrandit la forme pour l'adapter au texte. |
| [InternalMarginBottom](../../aspose.words.drawing/textbox/internalmarginbottom/) { get; set; } | Spécifie la marge inférieure intérieure en points pour une forme. |
| [InternalMarginLeft](../../aspose.words.drawing/textbox/internalmarginleft/) { get; set; } | Spécifie la marge intérieure gauche en points pour une forme. |
| [InternalMarginRight](../../aspose.words.drawing/textbox/internalmarginright/) { get; set; } | Spécifie la marge intérieure droite en points pour une forme. |
| [InternalMarginTop](../../aspose.words.drawing/textbox/internalmargintop/) { get; set; } | Spécifie la marge supérieure intérieure en points pour une forme. |
| [LayoutFlow](../../aspose.words.drawing/textbox/layoutflow/) { get; set; } | Détermine le flux de la disposition du texte dans une forme. |
| [Next](../../aspose.words.drawing/textbox/next/) { get; set; } | Renvoie ou définit un TextBox qui représente le TextBox suivant dans une séquence de formes. |
| [Parent](../../aspose.words.drawing/textbox/parent/) { get; } | Obtient une forme parent pour le TextBox. |
| [Previous](../../aspose.words.drawing/textbox/previous/) { get; } | Renvoie un TextBox qui représente le TextBox précédent dans une séquence de formes. |
| [TextBoxWrapMode](../../aspose.words.drawing/textbox/textboxwrapmode/) { get; set; } | Détermine comment le texte s'habille à l'intérieur d'une forme. |
| [VerticalAnchor](../../aspose.words.drawing/textbox/verticalanchor/) { get; set; } | Spécifie l'alignement vertical du texte dans une forme. |

## Méthodes

| Nom | La description |
| --- | --- |
| [BreakForwardLink](../../aspose.words.drawing/textbox/breakforwardlink/)() | Brise le lien vers le prochain TextBox. |
| [IsValidLinkTarget](../../aspose.words.drawing/textbox/isvalidlinktarget/)(TextBox) | Détermine si ce TextBox peut être lié au Textbox cible. |

### Remarques

Utilisez le[`TextBox`](../shape/textbox/) pour accéder aux propriétés de texte d'une forme. Vous ne créez pas d'instances de la`TextBox` classe directement.

### Exemples

Montre comment définir les marges internes d'une zone de texte.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère une autre zone de texte avec des marges spécifiques.
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

Montre comment définir l'orientation du texte dans une zone de texte.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Déplacez le générateur de document à l'intérieur du TextBox et ajoutez du texte.
builder.MoveTo(textBoxShape.LastParagraph);
builder.Writeln("Hello world!");
builder.Write("Hello again!");

// Définissez la propriété "LayoutFlow" pour définir une orientation pour le contenu textuel de cette zone de texte.
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

Montre comment faire en sorte qu'une zone de texte se redimensionne pour s'adapter parfaitement à son contenu.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Appliquez ces valeurs à ces deux membres pour que la forme parent s'adapte
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


