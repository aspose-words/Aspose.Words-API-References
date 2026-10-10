---
title: "TextBox"
linktitle: "TextBox"
second_title: "Aspose.Words für Java"
description: "Definiert Attribute, die festlegen, wie ein Text innerhalb einer Form in Java angezeigt wird."
type: docs
weight: 666
url: /de/java/com.aspose.words/textbox/
---

**Inheritance:**
java.lang.Object
```
public class TextBox
```

Definiert Attribute, die angeben, wie ein Text innerhalb einer Form angezeigt wird.

Um mehr zu erfahren, besuchen Sie den [ Working with Shapes ][Working with Shapes] Dokumentationsartikel.

 **Remarks:** 

Verwenden Sie die Eigenschaft [Shape.getTextBox()](../../com.aspose.words/shape/\\#getTextBox), um auf Texteigenschaften einer Form zuzugreifen. Sie erstellen keine Instanzen der Klasse [TextBox](../../com.aspose.words/textbox/) direkt.

 **Examples:** 

Zeigt, wie die Ausrichtung von Text innerhalb einer Textbox festgelegt wird.

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

Zeigt, wie eine Textbox sich selbst so verkleinert, dass ihr Inhalt eng passt.

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

Zeigt, wie interne Ränder für eine Textbox festgelegt werden.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [breakForwardLink()](#breakForwardLink) | Unterbricht die Verknüpfung zur nächsten [TextBox](../../com.aspose.words/textbox/). |
| [getFitShapeToText()](#getFitShapeToText) | Bestimmt, ob Microsoft Word die Form vergrößert, um den Text anzupassen. |
| [getInternalMarginBottom()](#getInternalMarginBottom) | Gibt den inneren unteren Rand in Punkten für eine Form an. |
| [getInternalMarginLeft()](#getInternalMarginLeft) | Gibt den inneren linken Rand in Punkten für eine Form an. |
| [getInternalMarginRight()](#getInternalMarginRight) | Gibt den inneren rechten Rand in Punkten für eine Form an. |
| [getInternalMarginTop()](#getInternalMarginTop) | Gibt den inneren oberen Rand in Punkten für eine Form an. |
| [getLayoutFlow()](#getLayoutFlow) | Bestimmt den Fluss des Textlayouts in einer Form. |
| [getNext()](#getNext) | Liefert eine [TextBox](../../com.aspose.words/textbox/), die die nächste [TextBox](../../com.aspose.words/textbox/) in einer Sequenz von Formen darstellt. |
| [getNoTextRotation()](#getNoTextRotation) | Liefert einen booleschen Wert, der angibt, ob der Text der TextBox nicht rotiert werden soll, wenn die Form rotiert wird. |
| [getParent()](#getParent) | Liefert eine übergeordnete Form für die [TextBox](../../com.aspose.words/textbox/). |
| [getPrevious()](#getPrevious) | Gibt eine [TextBox](../../com.aspose.words/textbox/) zurück, die die vorherige [TextBox](../../com.aspose.words/textbox/) in einer Sequenz von Formen darstellt. |
| [getTextBoxWrapMode()](#getTextBoxWrapMode) | Bestimmt, wie Text innerhalb einer Form umbrochen wird. |
| [getVerticalAnchor()](#getVerticalAnchor) | Gibt die vertikale Ausrichtung des Textes innerhalb einer Form an. |
| [isValidLinkTarget(TextBox target)](#isValidLinkTarget-com.aspose.words.TextBox) | Bestimmt, ob diese [TextBox](../../com.aspose.words/textbox/) mit der Ziel-[TextBox](../../com.aspose.words/textbox/) verknüpft werden kann. |
| [setFitShapeToText(boolean value)](#setFitShapeToText-boolean) | Bestimmt, ob Microsoft Word die Form vergrößert, um den Text anzupassen. |
| [setInternalMarginBottom(double value)](#setInternalMarginBottom-double) | Gibt den inneren unteren Rand in Punkten für eine Form an. |
| [setInternalMarginLeft(double value)](#setInternalMarginLeft-double) | Gibt den inneren linken Rand in Punkten für eine Form an. |
| [setInternalMarginRight(double value)](#setInternalMarginRight-double) | Gibt den inneren rechten Rand in Punkten für eine Form an. |
| [setInternalMarginTop(double value)](#setInternalMarginTop-double) | Gibt den inneren oberen Rand in Punkten für eine Form an. |
| [setLayoutFlow(int value)](#setLayoutFlow-int) | Bestimmt den Fluss des Textlayouts in einer Form. |
| [setNext(TextBox value)](#setNext-com.aspose.words.TextBox) | Setzt eine [TextBox](../../com.aspose.words/textbox/), die die nächste [TextBox](../../com.aspose.words/textbox/) in einer Sequenz von Formen darstellt. |
| [setNoTextRotation(boolean value)](#setNoTextRotation-boolean) | Setzt einen booleschen Wert, der angibt, ob der Text der TextBox nicht rotiert werden soll, wenn die Form rotiert wird. |
| [setTextBoxWrapMode(int value)](#setTextBoxWrapMode-int) | Bestimmt, wie Text innerhalb einer Form umbrochen wird. |
| [setVerticalAnchor(int value)](#setVerticalAnchor-int) | Gibt die vertikale Ausrichtung des Textes innerhalb einer Form an. |
### breakForwardLink() {#breakForwardLink}
```
public void breakForwardLink()
```


Unterbricht die Verknüpfung zur nächsten [TextBox](../../com.aspose.words/textbox/).

 **Remarks:** 

[breakForwardLink()](../../com.aspose.words/textbox/\#breakForwardLink) doesn't break all other links in the current sequence of shapes. For example: 1-2-3-4 sequence and [breakForwardLink()](../../com.aspose.words/textbox/\#breakForwardLink) at the 2-nd textbox will create two sequences 1-2, 3-4.

 **Examples:** 

Zeigt, wie Textboxen verknüpft werden.

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


Bestimmt, ob Microsoft Word die Form vergrößert, um den Text anzupassen.

 **Remarks:** 

Der Standardwert ist  false .

 **Examples:** 

Zeigt, wie eine Textbox sich selbst so verkleinert, dass ihr Inhalt eng passt.

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
boolean - Der entsprechende  boolean  Wert.
### getInternalMarginBottom() {#getInternalMarginBottom}
```
public double getInternalMarginBottom()
```


Gibt den inneren unteren Rand in Punkten für eine Form an.

 **Remarks:** 

Der Standardwert ist 1/20 Zoll.

 **Examples:** 

Zeigt, wie interne Ränder für eine Textbox festgelegt werden.

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
double - Der entsprechende  double  Wert.
### getInternalMarginLeft() {#getInternalMarginLeft}
```
public double getInternalMarginLeft()
```


Gibt den inneren linken Rand in Punkten für eine Form an.

 **Remarks:** 

Der Standardwert ist 1/10 Zoll.

 **Examples:** 

Zeigt, wie interne Ränder für eine Textbox festgelegt werden.

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
double - Der entsprechende  double  Wert.
### getInternalMarginRight() {#getInternalMarginRight}
```
public double getInternalMarginRight()
```


Gibt den inneren rechten Rand in Punkten für eine Form an.

 **Remarks:** 

Der Standardwert ist 1/10 Zoll.

 **Examples:** 

Zeigt, wie interne Ränder für eine Textbox festgelegt werden.

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
double - Der entsprechende  double  Wert.
### getInternalMarginTop() {#getInternalMarginTop}
```
public double getInternalMarginTop()
```


Gibt den inneren oberen Rand in Punkten für eine Form an.

 **Remarks:** 

Der Standardwert ist 1/20 Zoll.

 **Examples:** 

Zeigt, wie interne Ränder für eine Textbox festgelegt werden.

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
double - Der entsprechende  double  Wert.
### getLayoutFlow() {#getLayoutFlow}
```
public int getLayoutFlow()
```


Bestimmt den Fluss des Textlayouts in einer Form.

 **Remarks:** 

Der Standardwert ist [LayoutFlow.HORIZONTAL](../../com.aspose.words/layoutflow/\#HORIZONTAL).

 **Examples:** 

Zeigt, wie die Ausrichtung von Text innerhalb einer Textbox festgelegt wird.

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
int - Der entsprechende  int  Wert. Der zurückgegebene Wert ist einer der [LayoutFlow](../../com.aspose.words/layoutflow/) Konstanten.
### getNext() {#getNext}
```
public TextBox getNext()
```


Liefert eine [TextBox](../../com.aspose.words/textbox/), die die nächste [TextBox](../../com.aspose.words/textbox/) in einer Sequenz von Formen darstellt.

 **Examples:** 

Zeigt, wie Textboxen verknüpft werden.

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


Liefert einen booleschen Wert, der angibt, ob der Text der TextBox nicht rotiert werden soll, wenn die Form rotiert wird.

 **Remarks:** 

Der Standardwert ist  false

 **Examples:** 

Zeigt, wie die Textrotation deaktiviert wird, wenn die Form rotiert ist.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.ELLIPSE, 20.0, 20.0);
 shape.getTextBox().setNoTextRotation(true);

 doc.save(getArtifactsDir() + "Shape.NoTextRotation.docx");
 
```

**Returns:**
boolean - Ein boolescher Wert, der angibt, dass der Text der TextBox nicht rotiert werden soll, wenn die Form rotiert wird.
### getParent() {#getParent}
```
public Shape getParent()
```


Liefert eine übergeordnete Form für die [TextBox](../../com.aspose.words/textbox/).

**Returns:**
[Shape](../../com.aspose.words/shape/) - A parent shape for the [TextBox](../../com.aspose.words/textbox/).
### getPrevious() {#getPrevious}
```
public TextBox getPrevious()
```


Gibt eine [TextBox](../../com.aspose.words/textbox/) zurück, die die vorherige [TextBox](../../com.aspose.words/textbox/) in einer Sequenz von Formen darstellt.

 **Examples:** 

Zeigt, wie Textboxen verknüpft werden.

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


Bestimmt, wie Text innerhalb einer Form umbrochen wird.

 **Remarks:** 

Der Standardwert ist [TextBoxWrapMode.SQUARE](../../com.aspose.words/textboxwrapmode/\#SQUARE).

 **Examples:** 

Zeigt, wie ein Umbruchmodus für den Inhalt einer Textbox festgelegt wird.

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
int - Der entsprechende  int  Wert. Der zurückgegebene Wert ist einer der [TextBoxWrapMode](../../com.aspose.words/textboxwrapmode/) Konstanten.
### getVerticalAnchor() {#getVerticalAnchor}
```
public int getVerticalAnchor()
```


Gibt die vertikale Ausrichtung des Textes innerhalb einer Form an.

 **Remarks:** 

Der Standardwert ist [TextBoxAnchor.TOP](../../com.aspose.words/textboxanchor/\#TOP).

 **Examples:** 

Zeigt, wie der Textinhalt einer Textbox vertikal ausgerichtet wird.

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
int - Der entsprechende  int  Wert. Der zurückgegebene Wert ist einer der [TextBoxAnchor](../../com.aspose.words/textboxanchor/) Konstanten.
### isValidLinkTarget(TextBox target) {#isValidLinkTarget-com.aspose.words.TextBox}
```
public boolean isValidLinkTarget(TextBox target)
```


Bestimmt, ob diese [TextBox](../../com.aspose.words/textbox/) mit der Ziel-[TextBox](../../com.aspose.words/textbox/) verknüpft werden kann.

 **Examples:** 

Zeigt, wie Textboxen verknüpft werden.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| target | [TextBox](../../com.aspose.words/textbox/) |  |

**Returns:**
boolean
### setFitShapeToText(boolean value) {#setFitShapeToText-boolean}
```
public void setFitShapeToText(boolean value)
```


Bestimmt, ob Microsoft Word die Form vergrößert, um den Text anzupassen.

 **Remarks:** 

Der Standardwert ist  false .

 **Examples:** 

Zeigt, wie eine Textbox sich selbst so verkleinert, dass ihr Inhalt eng passt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setInternalMarginBottom(double value) {#setInternalMarginBottom-double}
```
public void setInternalMarginBottom(double value)
```


Gibt den inneren unteren Rand in Punkten für eine Form an.

 **Remarks:** 

Der Standardwert ist 1/20 Zoll.

 **Examples:** 

Zeigt, wie interne Ränder für eine Textbox festgelegt werden.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Der entsprechende  double  Wert. |

### setInternalMarginLeft(double value) {#setInternalMarginLeft-double}
```
public void setInternalMarginLeft(double value)
```


Gibt den inneren linken Rand in Punkten für eine Form an.

 **Remarks:** 

Der Standardwert ist 1/10 Zoll.

 **Examples:** 

Zeigt, wie interne Ränder für eine Textbox festgelegt werden.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Der entsprechende  double  Wert. |

### setInternalMarginRight(double value) {#setInternalMarginRight-double}
```
public void setInternalMarginRight(double value)
```


Gibt den inneren rechten Rand in Punkten für eine Form an.

 **Remarks:** 

Der Standardwert ist 1/10 Zoll.

 **Examples:** 

Zeigt, wie interne Ränder für eine Textbox festgelegt werden.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Der entsprechende  double  Wert. |

### setInternalMarginTop(double value) {#setInternalMarginTop-double}
```
public void setInternalMarginTop(double value)
```


Gibt den inneren oberen Rand in Punkten für eine Form an.

 **Remarks:** 

Der Standardwert ist 1/20 Zoll.

 **Examples:** 

Zeigt, wie interne Ränder für eine Textbox festgelegt werden.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Der entsprechende  double  Wert. |

### setLayoutFlow(int value) {#setLayoutFlow-int}
```
public void setLayoutFlow(int value)
```


Bestimmt den Fluss des Textlayouts in einer Form.

 **Remarks:** 

Der Standardwert ist [LayoutFlow.HORIZONTAL](../../com.aspose.words/layoutflow/\#HORIZONTAL).

 **Examples:** 

Zeigt, wie die Ausrichtung von Text innerhalb einer Textbox festgelegt wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende  int  Wert. Der Wert muss einer der [LayoutFlow](../../com.aspose.words/layoutflow/) Konstanten sein. |

### setNext(TextBox value) {#setNext-com.aspose.words.TextBox}
```
public void setNext(TextBox value)
```


Setzt eine [TextBox](../../com.aspose.words/textbox/), die die nächste [TextBox](../../com.aspose.words/textbox/) in einer Sequenz von Formen darstellt.

 **Examples:** 

Zeigt, wie Textboxen verknüpft werden.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | [TextBox](../../com.aspose.words/textbox/) | Eine [TextBox](../../com.aspose.words/textbox/), die die nächste [TextBox](../../com.aspose.words/textbox/) in einer Sequenz von Formen darstellt. |

### setNoTextRotation(boolean value) {#setNoTextRotation-boolean}
```
public void setNoTextRotation(boolean value)
```


Setzt einen booleschen Wert, der angibt, ob der Text der TextBox nicht rotiert werden soll, wenn die Form rotiert wird.

 **Remarks:** 

Der Standardwert ist  false

 **Examples:** 

Zeigt, wie die Textrotation deaktiviert wird, wenn die Form rotiert ist.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.ELLIPSE, 20.0, 20.0);
 shape.getTextBox().setNoTextRotation(true);

 doc.save(getArtifactsDir() + "Shape.NoTextRotation.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein boolescher Wert, der angibt, dass der Text der TextBox nicht rotiert werden soll, wenn die Form rotiert wird. |

### setTextBoxWrapMode(int value) {#setTextBoxWrapMode-int}
```
public void setTextBoxWrapMode(int value)
```


Bestimmt, wie Text innerhalb einer Form umbrochen wird.

 **Remarks:** 

Der Standardwert ist [TextBoxWrapMode.SQUARE](../../com.aspose.words/textboxwrapmode/\#SQUARE).

 **Examples:** 

Zeigt, wie ein Umbruchmodus für den Inhalt einer Textbox festgelegt wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende  int  Wert. Der Wert muss einer der [TextBoxWrapMode](../../com.aspose.words/textboxwrapmode/) Konstanten sein. |

### setVerticalAnchor(int value) {#setVerticalAnchor-int}
```
public void setVerticalAnchor(int value)
```


Gibt die vertikale Ausrichtung des Textes innerhalb einer Form an.

 **Remarks:** 

Der Standardwert ist [TextBoxAnchor.TOP](../../com.aspose.words/textboxanchor/\#TOP).

 **Examples:** 

Zeigt, wie der Textinhalt einer Textbox vertikal ausgerichtet wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende  int  Wert. Der Wert muss einer der [TextBoxAnchor](../../com.aspose.words/textboxanchor/) Konstanten sein. |

