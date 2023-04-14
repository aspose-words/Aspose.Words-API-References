---
title: TextBox
linktitle: TextBox
second_title: Aspose.Words for Java API Reference
description: Defines attributes that specify how a text is displayed inside a shape in Java.
type: docs
weight: 567
url: /java/com.aspose.words/textbox/
---

**Inheritance:**
java.lang.Object
```
public class TextBox
```

Defines attributes that specify how a text is displayed inside a shape.

To learn more, visit the [ Working with Shapes ][Working with Shapes] documentation article.

 **Remarks:** 

Use the [Shape.getTextBox()](../../com.aspose.words/shape/\#getTextBox) property to access text properties of a shape. You do not create instances of the [TextBox](../../com.aspose.words/textbox/) class directly.

 **Examples:** 

Shows how to set internal margins for a text box.

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

Shows how to set the orientation of text inside a text box.

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

Shows how to get a text box to resize itself to fit its contents tightly.

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


[Working with Shapes]: https://docs.aspose.com/words/java/working-with-shapes/
## Methods

| Method | Description |
| --- | --- |
| [breakForwardLink()](#breakForwardLink) | Breaks the link to the next [TextBox](../../com.aspose.words/textbox/). |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getFitShapeToText()](#getFitShapeToText) | Determines whether Microsoft Word will grow the shape to fit text. |
| [getInternalMarginBottom()](#getInternalMarginBottom) | Specifies the inner bottom margin in points for a shape. |
| [getInternalMarginLeft()](#getInternalMarginLeft) | Specifies the inner left margin in points for a shape. |
| [getInternalMarginRight()](#getInternalMarginRight) | Specifies the inner right margin in points for a shape. |
| [getInternalMarginTop()](#getInternalMarginTop) | Specifies the inner top margin in points for a shape. |
| [getLayoutFlow()](#getLayoutFlow) | Determines the flow of the text layout in a shape. |
| [getNext()](#getNext) | Gets a [TextBox](../../com.aspose.words/textbox/) that represents the next [TextBox](../../com.aspose.words/textbox/) in a sequence of shapes. |
| [getNoTextRotation()](#getNoTextRotation) | Gets a boolean value indicating either text of the TextBox should not rotate when the shape is rotated. |
| [getParent()](#getParent) | Gets a parent shape for the [TextBox](../../com.aspose.words/textbox/). |
| [getPrevious()](#getPrevious) | Returns a [TextBox](../../com.aspose.words/textbox/) that represents the previous [TextBox](../../com.aspose.words/textbox/) in a sequence of shapes. |
| [getTextBoxWrapMode()](#getTextBoxWrapMode) | Determines how text wraps inside a shape. |
| [getVerticalAnchor()](#getVerticalAnchor) | Specifies the vertical alignment of the text within a shape. |
| [hashCode()](#hashCode) |  |
| [isValidLinkTarget(TextBox target)](#isValidLinkTarget-com.aspose.words.TextBox) | Determines whether this [TextBox](../../com.aspose.words/textbox/) can be linked to the target [TextBox](../../com.aspose.words/textbox/). |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setFitShapeToText(boolean value)](#setFitShapeToText-boolean) | Determines whether Microsoft Word will grow the shape to fit text. |
| [setInternalMarginBottom(double value)](#setInternalMarginBottom-double) | Specifies the inner bottom margin in points for a shape. |
| [setInternalMarginLeft(double value)](#setInternalMarginLeft-double) | Specifies the inner left margin in points for a shape. |
| [setInternalMarginRight(double value)](#setInternalMarginRight-double) | Specifies the inner right margin in points for a shape. |
| [setInternalMarginTop(double value)](#setInternalMarginTop-double) | Specifies the inner top margin in points for a shape. |
| [setLayoutFlow(int value)](#setLayoutFlow-int) | Determines the flow of the text layout in a shape. |
| [setNext(TextBox value)](#setNext-com.aspose.words.TextBox) | Sets a [TextBox](../../com.aspose.words/textbox/) that represents the next [TextBox](../../com.aspose.words/textbox/) in a sequence of shapes. |
| [setNoTextRotation(boolean value)](#setNoTextRotation-boolean) | Sets a boolean value indicating either text of the TextBox should not rotate when the shape is rotated. |
| [setTextBoxWrapMode(int value)](#setTextBoxWrapMode-int) | Determines how text wraps inside a shape. |
| [setVerticalAnchor(int value)](#setVerticalAnchor-int) | Specifies the vertical alignment of the text within a shape. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### breakForwardLink() {#breakForwardLink}
```
public void breakForwardLink()
```


Breaks the link to the next [TextBox](../../com.aspose.words/textbox/).

 **Remarks:** 

[breakForwardLink()](../../com.aspose.words/textbox/\#breakForwardLink) doesn't break all other links in the current sequence of shapes. For example: 1-2-3-4 sequence and [breakForwardLink()](../../com.aspose.words/textbox/\#breakForwardLink) at the 2-nd textbox will create two sequences 1-2, 3-4.

 **Examples:** 

Shows how to link text boxes.

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

### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getFitShapeToText() {#getFitShapeToText}
```
public boolean getFitShapeToText()
```


Determines whether Microsoft Word will grow the shape to fit text.

 **Remarks:** 

The default value is  false .

 **Examples:** 

Shows how to get a text box to resize itself to fit its contents tightly.

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
boolean - The corresponding  boolean  value.
### getInternalMarginBottom() {#getInternalMarginBottom}
```
public double getInternalMarginBottom()
```


Specifies the inner bottom margin in points for a shape.

 **Remarks:** 

The default value is 1/20 inch.

 **Examples:** 

Shows how to set internal margins for a text box.

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
double - The corresponding  double  value.
### getInternalMarginLeft() {#getInternalMarginLeft}
```
public double getInternalMarginLeft()
```


Specifies the inner left margin in points for a shape.

 **Remarks:** 

The default value is 1/10 inch.

 **Examples:** 

Shows how to set internal margins for a text box.

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
double - The corresponding  double  value.
### getInternalMarginRight() {#getInternalMarginRight}
```
public double getInternalMarginRight()
```


Specifies the inner right margin in points for a shape.

 **Remarks:** 

The default value is 1/10 inch.

 **Examples:** 

Shows how to set internal margins for a text box.

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
double - The corresponding  double  value.
### getInternalMarginTop() {#getInternalMarginTop}
```
public double getInternalMarginTop()
```


Specifies the inner top margin in points for a shape.

 **Remarks:** 

The default value is 1/20 inch.

 **Examples:** 

Shows how to set internal margins for a text box.

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
double - The corresponding  double  value.
### getLayoutFlow() {#getLayoutFlow}
```
public int getLayoutFlow()
```


Determines the flow of the text layout in a shape.

 **Remarks:** 

The default value is [LayoutFlow.HORIZONTAL](../../com.aspose.words/layoutflow/\#HORIZONTAL).

 **Examples:** 

Shows how to set the orientation of text inside a text box.

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
int - The corresponding  int  value. The returned value is one of [LayoutFlow](../../com.aspose.words/layoutflow/) constants.
### getNext() {#getNext}
```
public TextBox getNext()
```


Gets a [TextBox](../../com.aspose.words/textbox/) that represents the next [TextBox](../../com.aspose.words/textbox/) in a sequence of shapes.

 **Examples:** 

Shows how to link text boxes.

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


Gets a boolean value indicating either text of the TextBox should not rotate when the shape is rotated.

 **Remarks:** 

The default value is  false 

 **Examples:** 

Shows how to disable text rotation when the shape is rotate.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.ELLIPSE, 20.0, 20.0);
 shape.getTextBox().setNoTextRotation(true);

 doc.save(getArtifactsDir() + "Shape.NoTextRotation.docx");
 
```

**Returns:**
boolean - A boolean value indicating either text of the TextBox should not rotate when the shape is rotated.
### getParent() {#getParent}
```
public Shape getParent()
```


Gets a parent shape for the [TextBox](../../com.aspose.words/textbox/).

**Returns:**
[Shape](../../com.aspose.words/shape/) - A parent shape for the [TextBox](../../com.aspose.words/textbox/).
### getPrevious() {#getPrevious}
```
public TextBox getPrevious()
```


Returns a [TextBox](../../com.aspose.words/textbox/) that represents the previous [TextBox](../../com.aspose.words/textbox/) in a sequence of shapes.

 **Examples:** 

Shows how to link text boxes.

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


Determines how text wraps inside a shape.

 **Remarks:** 

The default value is [TextBoxWrapMode.SQUARE](../../com.aspose.words/textboxwrapmode/\#SQUARE).

 **Examples:** 

Shows how to set a wrapping mode for the contents of a text box.

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
int - The corresponding  int  value. The returned value is one of [TextBoxWrapMode](../../com.aspose.words/textboxwrapmode/) constants.
### getVerticalAnchor() {#getVerticalAnchor}
```
public int getVerticalAnchor()
```


Specifies the vertical alignment of the text within a shape.

 **Remarks:** 

The default value is [TextBoxAnchor.TOP](../../com.aspose.words/textboxanchor/\#TOP).

 **Examples:** 

Shows how to vertically align the text contents of a text box.

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
int - The corresponding  int  value. The returned value is one of [TextBoxAnchor](../../com.aspose.words/textboxanchor/) constants.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### isValidLinkTarget(TextBox target) {#isValidLinkTarget-com.aspose.words.TextBox}
```
public boolean isValidLinkTarget(TextBox target)
```


Determines whether this [TextBox](../../com.aspose.words/textbox/) can be linked to the target [TextBox](../../com.aspose.words/textbox/).

 **Examples:** 

Shows how to link text boxes.

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
| Parameter | Type | Description |
| --- | --- | --- |
| target | [TextBox](../../com.aspose.words/textbox/) |  |

**Returns:**
boolean
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### setFitShapeToText(boolean value) {#setFitShapeToText-boolean}
```
public void setFitShapeToText(boolean value)
```


Determines whether Microsoft Word will grow the shape to fit text.

 **Remarks:** 

The default value is  false .

 **Examples:** 

Shows how to get a text box to resize itself to fit its contents tightly.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setInternalMarginBottom(double value) {#setInternalMarginBottom-double}
```
public void setInternalMarginBottom(double value)
```


Specifies the inner bottom margin in points for a shape.

 **Remarks:** 

The default value is 1/20 inch.

 **Examples:** 

Shows how to set internal margins for a text box.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The corresponding  double  value. |

### setInternalMarginLeft(double value) {#setInternalMarginLeft-double}
```
public void setInternalMarginLeft(double value)
```


Specifies the inner left margin in points for a shape.

 **Remarks:** 

The default value is 1/10 inch.

 **Examples:** 

Shows how to set internal margins for a text box.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The corresponding  double  value. |

### setInternalMarginRight(double value) {#setInternalMarginRight-double}
```
public void setInternalMarginRight(double value)
```


Specifies the inner right margin in points for a shape.

 **Remarks:** 

The default value is 1/10 inch.

 **Examples:** 

Shows how to set internal margins for a text box.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The corresponding  double  value. |

### setInternalMarginTop(double value) {#setInternalMarginTop-double}
```
public void setInternalMarginTop(double value)
```


Specifies the inner top margin in points for a shape.

 **Remarks:** 

The default value is 1/20 inch.

 **Examples:** 

Shows how to set internal margins for a text box.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The corresponding  double  value. |

### setLayoutFlow(int value) {#setLayoutFlow-int}
```
public void setLayoutFlow(int value)
```


Determines the flow of the text layout in a shape.

 **Remarks:** 

The default value is [LayoutFlow.HORIZONTAL](../../com.aspose.words/layoutflow/\#HORIZONTAL).

 **Examples:** 

Shows how to set the orientation of text inside a text box.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [LayoutFlow](../../com.aspose.words/layoutflow/) constants. |

### setNext(TextBox value) {#setNext-com.aspose.words.TextBox}
```
public void setNext(TextBox value)
```


Sets a [TextBox](../../com.aspose.words/textbox/) that represents the next [TextBox](../../com.aspose.words/textbox/) in a sequence of shapes.

 **Examples:** 

Shows how to link text boxes.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | [TextBox](../../com.aspose.words/textbox/) | A [TextBox](../../com.aspose.words/textbox/) that represents the next [TextBox](../../com.aspose.words/textbox/) in a sequence of shapes. |

### setNoTextRotation(boolean value) {#setNoTextRotation-boolean}
```
public void setNoTextRotation(boolean value)
```


Sets a boolean value indicating either text of the TextBox should not rotate when the shape is rotated.

 **Remarks:** 

The default value is  false 

 **Examples:** 

Shows how to disable text rotation when the shape is rotate.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.ELLIPSE, 20.0, 20.0);
 shape.getTextBox().setNoTextRotation(true);

 doc.save(getArtifactsDir() + "Shape.NoTextRotation.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value indicating either text of the TextBox should not rotate when the shape is rotated. |

### setTextBoxWrapMode(int value) {#setTextBoxWrapMode-int}
```
public void setTextBoxWrapMode(int value)
```


Determines how text wraps inside a shape.

 **Remarks:** 

The default value is [TextBoxWrapMode.SQUARE](../../com.aspose.words/textboxwrapmode/\#SQUARE).

 **Examples:** 

Shows how to set a wrapping mode for the contents of a text box.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [TextBoxWrapMode](../../com.aspose.words/textboxwrapmode/) constants. |

### setVerticalAnchor(int value) {#setVerticalAnchor-int}
```
public void setVerticalAnchor(int value)
```


Specifies the vertical alignment of the text within a shape.

 **Remarks:** 

The default value is [TextBoxAnchor.TOP](../../com.aspose.words/textboxanchor/\#TOP).

 **Examples:** 

Shows how to vertically align the text contents of a text box.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [TextBoxAnchor](../../com.aspose.words/textboxanchor/) constants. |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

