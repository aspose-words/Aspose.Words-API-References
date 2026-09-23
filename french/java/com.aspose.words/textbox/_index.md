---
title: "TextBox"
linktitle: "TextBox"
second_title: "Aspose.Words pour Java"
description: "Définit les attributs qui spécifient comment un texte est affiché à l'intérieur d'une forme en Java."
type: docs
weight: 666
url: /fr/java/com.aspose.words/textbox/
---

**Inheritance:**
java.lang.Object
```
public class TextBox
```

Définit les attributs qui spécifient comment un texte est affiché à l'intérieur d'une forme.

Pour en savoir plus, consultez l'article de documentation [ Working with Shapes ][Working with Shapes].

 **Remarks:** 

Utilisez la propriété [Shape.getTextBox()](../../com.aspose.words/shape/\#getTextBox) pour accéder aux propriétés de texte d'une forme. Vous ne créez pas d'instances de la classe [TextBox](../../com.aspose.words/textbox/) directement.

 **Examples:** 

Montre comment définir l'orientation du texte à l'intérieur d'une zone de texte.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape textBoxShape = builder.insertShape(ShapeType.TEXT_BOX, 150.0, 100.0);
 TextBox textBox = textBoxShape.getTextBox();

 // Move the document builder to inside the TextBox and add text.
 builder.moveTo(textBoxShape.getLastParagraph());
 builder.writeln("Hello world!");
 builder.write("Hello again!");

 // Set the "LayoutFlow" property to set an orientation for the text contents of this text box.
 textBox.setLayoutFlow(layoutFlow);

 doc.save(getArtifactsDir() + "Shape.TextBoxLayoutFlow.docx");
 
```

Montre comment faire en sorte qu'une zone de texte se redimensionne automatiquement pour ajuster étroitement son contenu.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape textBoxShape = builder.insertShape(ShapeType.TEXT_BOX, 150.0, 100.0);
 TextBox textBox = textBoxShape.getTextBox();

 // Apply these values to both these members to get the parent shape to fit
 // tightly around the text contents, ignoring the dimensions we have set.
 textBox.setFitShapeToText(true);
 textBox.setTextBoxWrapMode(TextBoxWrapMode.NONE);

 builder.moveTo(textBoxShape.getLastParagraph());
 builder.write("Text fit tightly inside textbox.");

 doc.save(getArtifactsDir() + "Shape.TextBoxFitShapeToText.docx");
 
```

Montre comment définir les marges internes d'une zone de texte.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert another textbox with specific margins.
 Shape textBoxShape = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 100.0);
 TextBox textBox = textBoxShape.getTextBox();
 textBox.setInternalMarginTop(15.0);
 textBox.setInternalMarginBottom(15.0);
 textBox.setInternalMarginLeft(15.0);
 textBox.setInternalMarginRight(15.0);

 builder.moveTo(textBoxShape.getLastParagraph());
 builder.write("Text placed according to textbox margins.");

 doc.save(getArtifactsDir() + "Shape.TextBoxMargins.docx");
 
```


[Working with Shapes]: https://docs.aspose.com/words/java/working-with-shapes/
## Méthodes

| Méthode | Description |
| --- | --- |
| [breakForwardLink()](#breakForwardLink) | Rompt le lien vers la prochaine [TextBox](../../com.aspose.words/textbox/). |
| [getFitShapeToText()](#getFitShapeToText) | Détermine si Microsoft Word agrandira la forme pour ajuster le texte. |
| [getInternalMarginBottom()](#getInternalMarginBottom) | Spécifie la marge intérieure inférieure en points pour une forme. |
| [getInternalMarginLeft()](#getInternalMarginLeft) | Spécifie la marge intérieure gauche en points pour une forme. |
| [getInternalMarginRight()](#getInternalMarginRight) | Spécifie la marge intérieure droite en points pour une forme. |
| [getInternalMarginTop()](#getInternalMarginTop) | Spécifie la marge intérieure supérieure en points pour une forme. |
| [getLayoutFlow()](#getLayoutFlow) | Détermine le flux de la mise en page du texte dans une forme. |
| [getNext()](#getNext) | Obtient une [TextBox](../../com.aspose.words/textbox/) qui représente la prochaine [TextBox](../../com.aspose.words/textbox/) dans une séquence de formes. |
| [getNoTextRotation()](#getNoTextRotation) | Obtient une valeur booléenne indiquant que le texte de la TextBox ne doit pas pivoter lorsque la forme est tournée. |
| [getParent()](#getParent) | Obtient une forme parent pour la [TextBox](../../com.aspose.words/textbox/). |
| [getPrevious()](#getPrevious) | Renvoie une [TextBox](../../com.aspose.words/textbox/) qui représente la [TextBox](../../com.aspose.words/textbox/) précédente dans une séquence de formes. |
| [getTextBoxWrapMode()](#getTextBoxWrapMode) | Détermine comment le texte s'enroule à l'intérieur d'une forme. |
| [getVerticalAnchor()](#getVerticalAnchor) | Spécifie l'alignement vertical du texte à l'intérieur d'une forme. |
| [isValidLinkTarget(TextBox target)](#isValidLinkTarget-com.aspose.words.TextBox) | Détermine si cette [TextBox](../../com.aspose.words/textbox/) peut être liée à la [TextBox](../../com.aspose.words/textbox/) cible. |
| [setFitShapeToText(boolean value)](#setFitShapeToText-boolean) | Détermine si Microsoft Word agrandira la forme pour ajuster le texte. |
| [setInternalMarginBottom(double value)](#setInternalMarginBottom-double) | Spécifie la marge intérieure inférieure en points pour une forme. |
| [setInternalMarginLeft(double value)](#setInternalMarginLeft-double) | Spécifie la marge intérieure gauche en points pour une forme. |
| [setInternalMarginRight(double value)](#setInternalMarginRight-double) | Spécifie la marge intérieure droite en points pour une forme. |
| [setInternalMarginTop(double value)](#setInternalMarginTop-double) | Spécifie la marge intérieure supérieure en points pour une forme. |
| [setLayoutFlow(int value)](#setLayoutFlow-int) | Détermine le flux de la mise en page du texte dans une forme. |
| [setNext(TextBox value)](#setNext-com.aspose.words.TextBox) | Définit une [TextBox](../../com.aspose.words/textbox/) qui représente la prochaine [TextBox](../../com.aspose.words/textbox/) dans une séquence de formes. |
| [setNoTextRotation(boolean value)](#setNoTextRotation-boolean) | Définit une valeur booléenne indiquant que le texte de la TextBox ne doit pas pivoter lorsque la forme est tournée. |
| [setTextBoxWrapMode(int value)](#setTextBoxWrapMode-int) | Détermine comment le texte s'enroule à l'intérieur d'une forme. |
| [setVerticalAnchor(int value)](#setVerticalAnchor-int) | Spécifie l'alignement vertical du texte à l'intérieur d'une forme. |
### breakForwardLink() {#breakForwardLink}
```
public void breakForwardLink()
```


Rompt le lien vers la prochaine [TextBox](../../com.aspose.words/textbox/).

 **Remarks:** 

[breakForwardLink()](../../com.aspose.words/textbox/\#breakForwardLink) doesn't break all other links in the current sequence of shapes. For example: 1-2-3-4 sequence and [breakForwardLink()](../../com.aspose.words/textbox/\#breakForwardLink) at the 2-nd textbox will create two sequences 1-2, 3-4.

 **Examples:** 

Montre comment lier des zones de texte.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape textBoxShape1 = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 100.0);
 TextBox textBox1 = textBoxShape1.getTextBox();
 builder.writeln();

 Shape textBoxShape2 = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 100.0);
 TextBox textBox2 = textBoxShape2.getTextBox();
 builder.writeln();

 Shape textBoxShape3 = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 100.0);
 TextBox textBox3 = textBoxShape3.getTextBox();
 builder.writeln();

 Shape textBoxShape4 = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 100.0);
 TextBox textBox4 = textBoxShape4.getTextBox();

 // Create links between some of the text boxes.
 if (textBox1.isValidLinkTarget(textBox2))
     textBox1.setNext(textBox2);

 if (textBox2.isValidLinkTarget(textBox3))
     textBox2.setNext(textBox3);

 // Only an empty text box may have a link.
 Assert.assertTrue(textBox3.isValidLinkTarget(textBox4));

 builder.moveTo(textBoxShape4.getLastParagraph());
 builder.write("Hello world!");

 Assert.assertFalse(textBox3.isValidLinkTarget(textBox4));

 if (textBox1.getNext() != null && textBox1.getPrevious() == null)
     System.out.println("This TextBox is the head of the sequence");

 if (textBox2.getNext() != null && textBox2.getPrevious() != null)
     System.out.println("This TextBox is the middle of the sequence");

 if (textBox3.getNext() == null && textBox3.getPrevious() != null) {
     System.out.println("This TextBox is the tail of the sequence");

     // Break the forward link between textBox2 and textBox3, and then verify that they are no longer linked.
     textBox3.getPrevious().breakForwardLink();

     Assert.assertTrue(textBox2.getNext() == null);
     Assert.assertTrue(textBox3.getPrevious() == null);
 }

 doc.save(getArtifactsDir() + "Shape.CreateLinkBetweenTextBoxes.docx");
 
```

### getFitShapeToText() {#getFitShapeToText}
```
public boolean getFitShapeToText()
```


Détermine si Microsoft Word agrandira la forme pour ajuster le texte.

 **Remarks:** 

La valeur par défaut est false.

 **Examples:** 

Montre comment faire en sorte qu'une zone de texte se redimensionne automatiquement pour ajuster étroitement son contenu.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape textBoxShape = builder.insertShape(ShapeType.TEXT_BOX, 150.0, 100.0);
 TextBox textBox = textBoxShape.getTextBox();

 // Apply these values to both these members to get the parent shape to fit
 // tightly around the text contents, ignoring the dimensions we have set.
 textBox.setFitShapeToText(true);
 textBox.setTextBoxWrapMode(TextBoxWrapMode.NONE);

 builder.moveTo(textBoxShape.getLastParagraph());
 builder.write("Text fit tightly inside textbox.");

 doc.save(getArtifactsDir() + "Shape.TextBoxFitShapeToText.docx");
 
```

**Returns:**
boolean - La valeur  boolean  correspondante.
### getInternalMarginBottom() {#getInternalMarginBottom}
```
public double getInternalMarginBottom()
```


Spécifie la marge intérieure inférieure en points pour une forme.

 **Remarks:** 

La valeur par défaut est 1/20 pouce.

 **Examples:** 

Montre comment définir les marges internes d'une zone de texte.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert another textbox with specific margins.
 Shape textBoxShape = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 100.0);
 TextBox textBox = textBoxShape.getTextBox();
 textBox.setInternalMarginTop(15.0);
 textBox.setInternalMarginBottom(15.0);
 textBox.setInternalMarginLeft(15.0);
 textBox.setInternalMarginRight(15.0);

 builder.moveTo(textBoxShape.getLastParagraph());
 builder.write("Text placed according to textbox margins.");

 doc.save(getArtifactsDir() + "Shape.TextBoxMargins.docx");
 
```

**Returns:**
double - La valeur  double  correspondante.
### getInternalMarginLeft() {#getInternalMarginLeft}
```
public double getInternalMarginLeft()
```


Spécifie la marge intérieure gauche en points pour une forme.

 **Remarks:** 

La valeur par défaut est 1/10 pouce.

 **Examples:** 

Montre comment définir les marges internes d'une zone de texte.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert another textbox with specific margins.
 Shape textBoxShape = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 100.0);
 TextBox textBox = textBoxShape.getTextBox();
 textBox.setInternalMarginTop(15.0);
 textBox.setInternalMarginBottom(15.0);
 textBox.setInternalMarginLeft(15.0);
 textBox.setInternalMarginRight(15.0);

 builder.moveTo(textBoxShape.getLastParagraph());
 builder.write("Text placed according to textbox margins.");

 doc.save(getArtifactsDir() + "Shape.TextBoxMargins.docx");
 
```

**Returns:**
double - La valeur  double  correspondante.
### getInternalMarginRight() {#getInternalMarginRight}
```
public double getInternalMarginRight()
```


Spécifie la marge intérieure droite en points pour une forme.

 **Remarks:** 

La valeur par défaut est 1/10 pouce.

 **Examples:** 

Montre comment définir les marges internes d'une zone de texte.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert another textbox with specific margins.
 Shape textBoxShape = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 100.0);
 TextBox textBox = textBoxShape.getTextBox();
 textBox.setInternalMarginTop(15.0);
 textBox.setInternalMarginBottom(15.0);
 textBox.setInternalMarginLeft(15.0);
 textBox.setInternalMarginRight(15.0);

 builder.moveTo(textBoxShape.getLastParagraph());
 builder.write("Text placed according to textbox margins.");

 doc.save(getArtifactsDir() + "Shape.TextBoxMargins.docx");
 
```

**Returns:**
double - La valeur  double  correspondante.
### getInternalMarginTop() {#getInternalMarginTop}
```
public double getInternalMarginTop()
```


Spécifie la marge intérieure supérieure en points pour une forme.

 **Remarks:** 

La valeur par défaut est 1/20 pouce.

 **Examples:** 

Montre comment définir les marges internes d'une zone de texte.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert another textbox with specific margins.
 Shape textBoxShape = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 100.0);
 TextBox textBox = textBoxShape.getTextBox();
 textBox.setInternalMarginTop(15.0);
 textBox.setInternalMarginBottom(15.0);
 textBox.setInternalMarginLeft(15.0);
 textBox.setInternalMarginRight(15.0);

 builder.moveTo(textBoxShape.getLastParagraph());
 builder.write("Text placed according to textbox margins.");

 doc.save(getArtifactsDir() + "Shape.TextBoxMargins.docx");
 
```

**Returns:**
double - La valeur  double  correspondante.
### getLayoutFlow() {#getLayoutFlow}
```
public int getLayoutFlow()
```


Détermine le flux de la mise en page du texte dans une forme.

 **Remarks:** 

La valeur par défaut est [LayoutFlow.HORIZONTAL](../../com.aspose.words/layoutflow/\#HORIZONTAL).

 **Examples:** 

Montre comment définir l'orientation du texte à l'intérieur d'une zone de texte.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape textBoxShape = builder.insertShape(ShapeType.TEXT_BOX, 150.0, 100.0);
 TextBox textBox = textBoxShape.getTextBox();

 // Move the document builder to inside the TextBox and add text.
 builder.moveTo(textBoxShape.getLastParagraph());
 builder.writeln("Hello world!");
 builder.write("Hello again!");

 // Set the "LayoutFlow" property to set an orientation for the text contents of this text box.
 textBox.setLayoutFlow(layoutFlow);

 doc.save(getArtifactsDir() + "Shape.TextBoxLayoutFlow.docx");
 
```

**Returns:**
int - La valeur  int  correspondante. La valeur retournée est l'une des constantes [LayoutFlow](../../com.aspose.words/layoutflow/).
### getNext() {#getNext}
```
public TextBox getNext()
```


Obtient une [TextBox](../../com.aspose.words/textbox/) qui représente la prochaine [TextBox](../../com.aspose.words/textbox/) dans une séquence de formes.

 **Examples:** 

Montre comment lier des zones de texte.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape textBoxShape1 = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 100.0);
 TextBox textBox1 = textBoxShape1.getTextBox();
 builder.writeln();

 Shape textBoxShape2 = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 100.0);
 TextBox textBox2 = textBoxShape2.getTextBox();
 builder.writeln();

 Shape textBoxShape3 = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 100.0);
 TextBox textBox3 = textBoxShape3.getTextBox();
 builder.writeln();

 Shape textBoxShape4 = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 100.0);
 TextBox textBox4 = textBoxShape4.getTextBox();

 // Create links between some of the text boxes.
 if (textBox1.isValidLinkTarget(textBox2))
     textBox1.setNext(textBox2);

 if (textBox2.isValidLinkTarget(textBox3))
     textBox2.setNext(textBox3);

 // Only an empty text box may have a link.
 Assert.assertTrue(textBox3.isValidLinkTarget(textBox4));

 builder.moveTo(textBoxShape4.getLastParagraph());
 builder.write("Hello world!");

 Assert.assertFalse(textBox3.isValidLinkTarget(textBox4));

 if (textBox1.getNext() != null && textBox1.getPrevious() == null)
     System.out.println("This TextBox is the head of the sequence");

 if (textBox2.getNext() != null && textBox2.getPrevious() != null)
     System.out.println("This TextBox is the middle of the sequence");

 if (textBox3.getNext() == null && textBox3.getPrevious() != null) {
     System.out.println("This TextBox is the tail of the sequence");

     // Break the forward link between textBox2 and textBox3, and then verify that they are no longer linked.
     textBox3.getPrevious().breakForwardLink();

     Assert.assertTrue(textBox2.getNext() == null);
     Assert.assertTrue(textBox3.getPrevious() == null);
 }

 doc.save(getArtifactsDir() + "Shape.CreateLinkBetweenTextBoxes.docx");
 
```

**Returns:**
[TextBox](../../com.aspose.words/textbox/) - A [TextBox](../../com.aspose.words/textbox/) that represents the next [TextBox](../../com.aspose.words/textbox/) in a sequence of shapes.
### getNoTextRotation() {#getNoTextRotation}
```
public boolean getNoTextRotation()
```


Obtient une valeur booléenne indiquant que le texte de la TextBox ne doit pas pivoter lorsque la forme est tournée.

 **Remarks:** 

La valeur par défaut est  false

 **Examples:** 

Montre comment désactiver la rotation du texte lorsque la forme est pivotée.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.ELLIPSE, 20.0, 20.0);
 shape.getTextBox().setNoTextRotation(true);

 doc.save(getArtifactsDir() + "Shape.NoTextRotation.docx");
 
```

**Returns:**
boolean - Une valeur booléenne indiquant que le texte de la TextBox ne doit pas pivoter lorsque la forme est tournée.
### getParent() {#getParent}
```
public Shape getParent()
```


Obtient une forme parent pour la [TextBox](../../com.aspose.words/textbox/).

**Returns:**
[Shape](../../com.aspose.words/shape/) - A parent shape for the [TextBox](../../com.aspose.words/textbox/).
### getPrevious() {#getPrevious}
```
public TextBox getPrevious()
```


Renvoie une [TextBox](../../com.aspose.words/textbox/) qui représente la [TextBox](../../com.aspose.words/textbox/) précédente dans une séquence de formes.

 **Examples:** 

Montre comment lier des zones de texte.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape textBoxShape1 = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 100.0);
 TextBox textBox1 = textBoxShape1.getTextBox();
 builder.writeln();

 Shape textBoxShape2 = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 100.0);
 TextBox textBox2 = textBoxShape2.getTextBox();
 builder.writeln();

 Shape textBoxShape3 = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 100.0);
 TextBox textBox3 = textBoxShape3.getTextBox();
 builder.writeln();

 Shape textBoxShape4 = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 100.0);
 TextBox textBox4 = textBoxShape4.getTextBox();

 // Create links between some of the text boxes.
 if (textBox1.isValidLinkTarget(textBox2))
     textBox1.setNext(textBox2);

 if (textBox2.isValidLinkTarget(textBox3))
     textBox2.setNext(textBox3);

 // Only an empty text box may have a link.
 Assert.assertTrue(textBox3.isValidLinkTarget(textBox4));

 builder.moveTo(textBoxShape4.getLastParagraph());
 builder.write("Hello world!");

 Assert.assertFalse(textBox3.isValidLinkTarget(textBox4));

 if (textBox1.getNext() != null && textBox1.getPrevious() == null)
     System.out.println("This TextBox is the head of the sequence");

 if (textBox2.getNext() != null && textBox2.getPrevious() != null)
     System.out.println("This TextBox is the middle of the sequence");

 if (textBox3.getNext() == null && textBox3.getPrevious() != null) {
     System.out.println("This TextBox is the tail of the sequence");

     // Break the forward link between textBox2 and textBox3, and then verify that they are no longer linked.
     textBox3.getPrevious().breakForwardLink();

     Assert.assertTrue(textBox2.getNext() == null);
     Assert.assertTrue(textBox3.getPrevious() == null);
 }

 doc.save(getArtifactsDir() + "Shape.CreateLinkBetweenTextBoxes.docx");
 
```

**Returns:**
[TextBox](../../com.aspose.words/textbox/) - A [TextBox](../../com.aspose.words/textbox/) that represents the previous [TextBox](../../com.aspose.words/textbox/) in a sequence of shapes.
### getTextBoxWrapMode() {#getTextBoxWrapMode}
```
public int getTextBoxWrapMode()
```


Détermine comment le texte s'enroule à l'intérieur d'une forme.

 **Remarks:** 

La valeur par défaut est [TextBoxWrapMode.SQUARE](../../com.aspose.words/textboxwrapmode/\#SQUARE).

 **Examples:** 

Montre comment définir un mode d'habillage pour le contenu d'une zone de texte.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape textBoxShape = builder.insertShape(ShapeType.TEXT_BOX, 300.0, 300.0);
 TextBox textBox = textBoxShape.getTextBox();

 // Set the "TextBoxWrapMode" property to "TextBoxWrapMode.None" to increase the text box's width
 // to accommodate text, should it be large enough.
 // Set the "TextBoxWrapMode" property to "TextBoxWrapMode.Square" to
 // wrap all text inside the text box, preserving its dimensions.
 textBox.setTextBoxWrapMode(textBoxWrapMode);

 builder.moveTo(textBoxShape.getLastParagraph());
 builder.getFont().setSize(32.0);
 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.save(getArtifactsDir() + "Shape.TextBoxContentsWrapMode.docx");
 
```

**Returns:**
int - La valeur  int  correspondante. La valeur retournée est l'une des constantes [TextBoxWrapMode](../../com.aspose.words/textboxwrapmode/).
### getVerticalAnchor() {#getVerticalAnchor}
```
public int getVerticalAnchor()
```


Spécifie l'alignement vertical du texte à l'intérieur d'une forme.

 **Remarks:** 

La valeur par défaut est [TextBoxAnchor.TOP](../../com.aspose.words/textboxanchor/\#TOP).

 **Examples:** 

Montre comment aligner verticalement le texte d'une zone de texte.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.TEXT_BOX, 200.0, 200.0);

 // Set the "VerticalAnchor" property to "TextBoxAnchor.Top" to
 // align the text in this text box with the top side of the shape.
 // Set the "VerticalAnchor" property to "TextBoxAnchor.Middle" to
 // align the text in this text box to the center of the shape.
 // Set the "VerticalAnchor" property to "TextBoxAnchor.Bottom" to
 // align the text in this text box to the bottom of the shape.
 shape.getTextBox().setVerticalAnchor(verticalAnchor);

 builder.moveTo(shape.getFirstParagraph());
 builder.write("Hello world!");

 // The vertical aligning of text inside text boxes is available from Microsoft Word 2007 onwards.
 doc.getCompatibilityOptions().optimizeFor(MsWordVersion.WORD_2007);
 doc.save(getArtifactsDir() + "Shape.VerticalAnchor.docx");
 
```

**Returns:**
int - La valeur  int  correspondante. La valeur retournée est l'une des constantes [TextBoxAnchor](../../com.aspose.words/textboxanchor/).
### isValidLinkTarget(TextBox target) {#isValidLinkTarget-com.aspose.words.TextBox}
```
public boolean isValidLinkTarget(TextBox target)
```


Détermine si cette [TextBox](../../com.aspose.words/textbox/) peut être liée à la [TextBox](../../com.aspose.words/textbox/) cible.

 **Examples:** 

Montre comment lier des zones de texte.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape textBoxShape1 = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 100.0);
 TextBox textBox1 = textBoxShape1.getTextBox();
 builder.writeln();

 Shape textBoxShape2 = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 100.0);
 TextBox textBox2 = textBoxShape2.getTextBox();
 builder.writeln();

 Shape textBoxShape3 = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 100.0);
 TextBox textBox3 = textBoxShape3.getTextBox();
 builder.writeln();

 Shape textBoxShape4 = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 100.0);
 TextBox textBox4 = textBoxShape4.getTextBox();

 // Create links between some of the text boxes.
 if (textBox1.isValidLinkTarget(textBox2))
     textBox1.setNext(textBox2);

 if (textBox2.isValidLinkTarget(textBox3))
     textBox2.setNext(textBox3);

 // Only an empty text box may have a link.
 Assert.assertTrue(textBox3.isValidLinkTarget(textBox4));

 builder.moveTo(textBoxShape4.getLastParagraph());
 builder.write("Hello world!");

 Assert.assertFalse(textBox3.isValidLinkTarget(textBox4));

 if (textBox1.getNext() != null && textBox1.getPrevious() == null)
     System.out.println("This TextBox is the head of the sequence");

 if (textBox2.getNext() != null && textBox2.getPrevious() != null)
     System.out.println("This TextBox is the middle of the sequence");

 if (textBox3.getNext() == null && textBox3.getPrevious() != null) {
     System.out.println("This TextBox is the tail of the sequence");

     // Break the forward link between textBox2 and textBox3, and then verify that they are no longer linked.
     textBox3.getPrevious().breakForwardLink();

     Assert.assertTrue(textBox2.getNext() == null);
     Assert.assertTrue(textBox3.getPrevious() == null);
 }

 doc.save(getArtifactsDir() + "Shape.CreateLinkBetweenTextBoxes.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| target | [TextBox](../../com.aspose.words/textbox/) |  |

**Returns:**
boolean
### setFitShapeToText(boolean value) {#setFitShapeToText-boolean}
```
public void setFitShapeToText(boolean value)
```


Détermine si Microsoft Word agrandira la forme pour ajuster le texte.

 **Remarks:** 

La valeur par défaut est false.

 **Examples:** 

Montre comment faire en sorte qu'une zone de texte se redimensionne automatiquement pour ajuster étroitement son contenu.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape textBoxShape = builder.insertShape(ShapeType.TEXT_BOX, 150.0, 100.0);
 TextBox textBox = textBoxShape.getTextBox();

 // Apply these values to both these members to get the parent shape to fit
 // tightly around the text contents, ignoring the dimensions we have set.
 textBox.setFitShapeToText(true);
 textBox.setTextBoxWrapMode(TextBoxWrapMode.NONE);

 builder.moveTo(textBoxShape.getLastParagraph());
 builder.write("Text fit tightly inside textbox.");

 doc.save(getArtifactsDir() + "Shape.TextBoxFitShapeToText.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setInternalMarginBottom(double value) {#setInternalMarginBottom-double}
```
public void setInternalMarginBottom(double value)
```


Spécifie la marge intérieure inférieure en points pour une forme.

 **Remarks:** 

La valeur par défaut est 1/20 pouce.

 **Examples:** 

Montre comment définir les marges internes d'une zone de texte.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert another textbox with specific margins.
 Shape textBoxShape = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 100.0);
 TextBox textBox = textBoxShape.getTextBox();
 textBox.setInternalMarginTop(15.0);
 textBox.setInternalMarginBottom(15.0);
 textBox.setInternalMarginLeft(15.0);
 textBox.setInternalMarginRight(15.0);

 builder.moveTo(textBoxShape.getLastParagraph());
 builder.write("Text placed according to textbox margins.");

 doc.save(getArtifactsDir() + "Shape.TextBoxMargins.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | La valeur  double  correspondante. |

### setInternalMarginLeft(double value) {#setInternalMarginLeft-double}
```
public void setInternalMarginLeft(double value)
```


Spécifie la marge intérieure gauche en points pour une forme.

 **Remarks:** 

La valeur par défaut est 1/10 pouce.

 **Examples:** 

Montre comment définir les marges internes d'une zone de texte.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert another textbox with specific margins.
 Shape textBoxShape = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 100.0);
 TextBox textBox = textBoxShape.getTextBox();
 textBox.setInternalMarginTop(15.0);
 textBox.setInternalMarginBottom(15.0);
 textBox.setInternalMarginLeft(15.0);
 textBox.setInternalMarginRight(15.0);

 builder.moveTo(textBoxShape.getLastParagraph());
 builder.write("Text placed according to textbox margins.");

 doc.save(getArtifactsDir() + "Shape.TextBoxMargins.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | La valeur  double  correspondante. |

### setInternalMarginRight(double value) {#setInternalMarginRight-double}
```
public void setInternalMarginRight(double value)
```


Spécifie la marge intérieure droite en points pour une forme.

 **Remarks:** 

La valeur par défaut est 1/10 pouce.

 **Examples:** 

Montre comment définir les marges internes d'une zone de texte.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert another textbox with specific margins.
 Shape textBoxShape = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 100.0);
 TextBox textBox = textBoxShape.getTextBox();
 textBox.setInternalMarginTop(15.0);
 textBox.setInternalMarginBottom(15.0);
 textBox.setInternalMarginLeft(15.0);
 textBox.setInternalMarginRight(15.0);

 builder.moveTo(textBoxShape.getLastParagraph());
 builder.write("Text placed according to textbox margins.");

 doc.save(getArtifactsDir() + "Shape.TextBoxMargins.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | La valeur  double  correspondante. |

### setInternalMarginTop(double value) {#setInternalMarginTop-double}
```
public void setInternalMarginTop(double value)
```


Spécifie la marge intérieure supérieure en points pour une forme.

 **Remarks:** 

La valeur par défaut est 1/20 pouce.

 **Examples:** 

Montre comment définir les marges internes d'une zone de texte.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert another textbox with specific margins.
 Shape textBoxShape = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 100.0);
 TextBox textBox = textBoxShape.getTextBox();
 textBox.setInternalMarginTop(15.0);
 textBox.setInternalMarginBottom(15.0);
 textBox.setInternalMarginLeft(15.0);
 textBox.setInternalMarginRight(15.0);

 builder.moveTo(textBoxShape.getLastParagraph());
 builder.write("Text placed according to textbox margins.");

 doc.save(getArtifactsDir() + "Shape.TextBoxMargins.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | La valeur  double  correspondante. |

### setLayoutFlow(int value) {#setLayoutFlow-int}
```
public void setLayoutFlow(int value)
```


Détermine le flux de la mise en page du texte dans une forme.

 **Remarks:** 

La valeur par défaut est [LayoutFlow.HORIZONTAL](../../com.aspose.words/layoutflow/\#HORIZONTAL).

 **Examples:** 

Montre comment définir l'orientation du texte à l'intérieur d'une zone de texte.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape textBoxShape = builder.insertShape(ShapeType.TEXT_BOX, 150.0, 100.0);
 TextBox textBox = textBoxShape.getTextBox();

 // Move the document builder to inside the TextBox and add text.
 builder.moveTo(textBoxShape.getLastParagraph());
 builder.writeln("Hello world!");
 builder.write("Hello again!");

 // Set the "LayoutFlow" property to set an orientation for the text contents of this text box.
 textBox.setLayoutFlow(layoutFlow);

 doc.save(getArtifactsDir() + "Shape.TextBoxLayoutFlow.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | La valeur  int  correspondante. La valeur doit être l'une des constantes [LayoutFlow](../../com.aspose.words/layoutflow/). |

### setNext(TextBox value) {#setNext-com.aspose.words.TextBox}
```
public void setNext(TextBox value)
```


Définit une [TextBox](../../com.aspose.words/textbox/) qui représente la prochaine [TextBox](../../com.aspose.words/textbox/) dans une séquence de formes.

 **Examples:** 

Montre comment lier des zones de texte.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape textBoxShape1 = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 100.0);
 TextBox textBox1 = textBoxShape1.getTextBox();
 builder.writeln();

 Shape textBoxShape2 = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 100.0);
 TextBox textBox2 = textBoxShape2.getTextBox();
 builder.writeln();

 Shape textBoxShape3 = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 100.0);
 TextBox textBox3 = textBoxShape3.getTextBox();
 builder.writeln();

 Shape textBoxShape4 = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 100.0);
 TextBox textBox4 = textBoxShape4.getTextBox();

 // Create links between some of the text boxes.
 if (textBox1.isValidLinkTarget(textBox2))
     textBox1.setNext(textBox2);

 if (textBox2.isValidLinkTarget(textBox3))
     textBox2.setNext(textBox3);

 // Only an empty text box may have a link.
 Assert.assertTrue(textBox3.isValidLinkTarget(textBox4));

 builder.moveTo(textBoxShape4.getLastParagraph());
 builder.write("Hello world!");

 Assert.assertFalse(textBox3.isValidLinkTarget(textBox4));

 if (textBox1.getNext() != null && textBox1.getPrevious() == null)
     System.out.println("This TextBox is the head of the sequence");

 if (textBox2.getNext() != null && textBox2.getPrevious() != null)
     System.out.println("This TextBox is the middle of the sequence");

 if (textBox3.getNext() == null && textBox3.getPrevious() != null) {
     System.out.println("This TextBox is the tail of the sequence");

     // Break the forward link between textBox2 and textBox3, and then verify that they are no longer linked.
     textBox3.getPrevious().breakForwardLink();

     Assert.assertTrue(textBox2.getNext() == null);
     Assert.assertTrue(textBox3.getPrevious() == null);
 }

 doc.save(getArtifactsDir() + "Shape.CreateLinkBetweenTextBoxes.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | [TextBox](../../com.aspose.words/textbox/) | Un [TextBox](../../com.aspose.words/textbox/) qui représente le prochain [TextBox](../../com.aspose.words/textbox/) dans une séquence de formes. |

### setNoTextRotation(boolean value) {#setNoTextRotation-boolean}
```
public void setNoTextRotation(boolean value)
```


Définit une valeur booléenne indiquant que le texte de la TextBox ne doit pas pivoter lorsque la forme est tournée.

 **Remarks:** 

La valeur par défaut est  false

 **Examples:** 

Montre comment désactiver la rotation du texte lorsque la forme est pivotée.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.ELLIPSE, 20.0, 20.0);
 shape.getTextBox().setNoTextRotation(true);

 doc.save(getArtifactsDir() + "Shape.NoTextRotation.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | Une valeur booléenne indiquant que le texte de la TextBox ne doit pas pivoter lorsque la forme est tournée. |

### setTextBoxWrapMode(int value) {#setTextBoxWrapMode-int}
```
public void setTextBoxWrapMode(int value)
```


Détermine comment le texte s'enroule à l'intérieur d'une forme.

 **Remarks:** 

La valeur par défaut est [TextBoxWrapMode.SQUARE](../../com.aspose.words/textboxwrapmode/\#SQUARE).

 **Examples:** 

Montre comment définir un mode d'habillage pour le contenu d'une zone de texte.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape textBoxShape = builder.insertShape(ShapeType.TEXT_BOX, 300.0, 300.0);
 TextBox textBox = textBoxShape.getTextBox();

 // Set the "TextBoxWrapMode" property to "TextBoxWrapMode.None" to increase the text box's width
 // to accommodate text, should it be large enough.
 // Set the "TextBoxWrapMode" property to "TextBoxWrapMode.Square" to
 // wrap all text inside the text box, preserving its dimensions.
 textBox.setTextBoxWrapMode(textBoxWrapMode);

 builder.moveTo(textBoxShape.getLastParagraph());
 builder.getFont().setSize(32.0);
 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.save(getArtifactsDir() + "Shape.TextBoxContentsWrapMode.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | La valeur  int  correspondante. La valeur doit être l'une des constantes [TextBoxWrapMode](../../com.aspose.words/textboxwrapmode/). |

### setVerticalAnchor(int value) {#setVerticalAnchor-int}
```
public void setVerticalAnchor(int value)
```


Spécifie l'alignement vertical du texte à l'intérieur d'une forme.

 **Remarks:** 

La valeur par défaut est [TextBoxAnchor.TOP](../../com.aspose.words/textboxanchor/\#TOP).

 **Examples:** 

Montre comment aligner verticalement le texte d'une zone de texte.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.TEXT_BOX, 200.0, 200.0);

 // Set the "VerticalAnchor" property to "TextBoxAnchor.Top" to
 // align the text in this text box with the top side of the shape.
 // Set the "VerticalAnchor" property to "TextBoxAnchor.Middle" to
 // align the text in this text box to the center of the shape.
 // Set the "VerticalAnchor" property to "TextBoxAnchor.Bottom" to
 // align the text in this text box to the bottom of the shape.
 shape.getTextBox().setVerticalAnchor(verticalAnchor);

 builder.moveTo(shape.getFirstParagraph());
 builder.write("Hello world!");

 // The vertical aligning of text inside text boxes is available from Microsoft Word 2007 onwards.
 doc.getCompatibilityOptions().optimizeFor(MsWordVersion.WORD_2007);
 doc.save(getArtifactsDir() + "Shape.VerticalAnchor.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | La valeur  int  correspondante. La valeur doit être l'une des constantes [TextBoxAnchor](../../com.aspose.words/textboxanchor/). |

