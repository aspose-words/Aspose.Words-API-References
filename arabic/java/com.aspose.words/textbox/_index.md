---
title: "TextBox"
linktitle: "TextBox"
second_title: "Aspose.Words لـ Java"
description: "يحدد السمات التي تحدد كيفية عرض النص داخل شكل في Java."
type: docs
weight: 666
url: /ar/java/com.aspose.words/textbox/
---

**Inheritance:**
java.lang.Object
```
public class TextBox
```

يعرف السمات التي تحدد كيفية عرض النص داخل الشكل.

لمزيد من المعلومات، زر مقالة الوثائق [ Working with Shapes ][Working with Shapes].

 **Remarks:** 

استخدم الخاصية [Shape.getTextBox()](../../com.aspose.words/shape/\#getTextBox) للوصول إلى خصائص النص في الشكل. لا تقوم بإنشاء مثيلات من الفئة [TextBox](../../com.aspose.words/textbox/) مباشرةً.

 **Examples:** 

يعرض كيفية تعيين اتجاه النص داخل مربع النص.

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

يعرض كيفية جعل مربع النص يعيد تحجيم نفسه ليتناسب بإحكام مع محتوياته.

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

يعرض كيفية تعيين الهوامش الداخلية لمربع النص.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [breakForwardLink()](#breakForwardLink) | يفصل الرابط إلى الـ [TextBox](../../com.aspose.words/textbox/) التالي. |
| [getFitShapeToText()](#getFitShapeToText) | يحدد ما إذا كان Microsoft Word سيزيد حجم الشكل ليتناسب مع النص. |
| [getInternalMarginBottom()](#getInternalMarginBottom) | يحدد الهامش الداخلي السفلي بالنقاط لشكل. |
| [getInternalMarginLeft()](#getInternalMarginLeft) | يحدد الهامش الداخلي الأيسر بالنقاط لشكل. |
| [getInternalMarginRight()](#getInternalMarginRight) | يحدد الهامش الداخلي الأيمن بالنقاط لشكل. |
| [getInternalMarginTop()](#getInternalMarginTop) | يحدد الهامش الداخلي العلوي بالنقاط لشكل. |
| [getLayoutFlow()](#getLayoutFlow) | يحدد تدفق تخطيط النص داخل الشكل. |
| [getNext()](#getNext) | يحصل على [TextBox](../../com.aspose.words/textbox/) الذي يمثل الـ [TextBox](../../com.aspose.words/textbox/) التالي في تسلسل الأشكال. |
| [getNoTextRotation()](#getNoTextRotation) | يحصل على قيمة منطقية تشير إلى ما إذا كان نص الـ TextBox يجب ألا يدور عندما يتم تدوير الشكل. |
| [getParent()](#getParent) | يحصل على الشكل الأب للـ [TextBox](../../com.aspose.words/textbox/). |
| [getPrevious()](#getPrevious) | يعيد [TextBox](../../com.aspose.words/textbox/) الذي يمثل الـ [TextBox](../../com.aspose.words/textbox/) السابق في تسلسل الأشكال. |
| [getTextBoxWrapMode()](#getTextBoxWrapMode) | يحدد كيفية التفاف النص داخل الشكل. |
| [getVerticalAnchor()](#getVerticalAnchor) | يحدد محاذاة النص العمودية داخل الشكل. |
| [isValidLinkTarget(TextBox target)](#isValidLinkTarget-com.aspose.words.TextBox) | يحدد ما إذا كان يمكن ربط هذا الـ [TextBox](../../com.aspose.words/textbox/) بـ [TextBox](../../com.aspose.words/textbox/) الهدف. |
| [setFitShapeToText(boolean value)](#setFitShapeToText-boolean) | يحدد ما إذا كان Microsoft Word سيزيد حجم الشكل ليتناسب مع النص. |
| [setInternalMarginBottom(double value)](#setInternalMarginBottom-double) | يحدد الهامش الداخلي السفلي بالنقاط لشكل. |
| [setInternalMarginLeft(double value)](#setInternalMarginLeft-double) | يحدد الهامش الداخلي الأيسر بالنقاط لشكل. |
| [setInternalMarginRight(double value)](#setInternalMarginRight-double) | يحدد الهامش الداخلي الأيمن بالنقاط لشكل. |
| [setInternalMarginTop(double value)](#setInternalMarginTop-double) | يحدد الهامش الداخلي العلوي بالنقاط لشكل. |
| [setLayoutFlow(int value)](#setLayoutFlow-int) | يحدد تدفق تخطيط النص داخل الشكل. |
| [setNext(TextBox value)](#setNext-com.aspose.words.TextBox) | يضبط [TextBox](../../com.aspose.words/textbox/) الذي يمثل الـ [TextBox](../../com.aspose.words/textbox/) التالي في تسلسل الأشكال. |
| [setNoTextRotation(boolean value)](#setNoTextRotation-boolean) | يضبط قيمة منطقية تشير إلى ما إذا كان نص الـ TextBox يجب ألا يدور عندما يتم تدوير الشكل. |
| [setTextBoxWrapMode(int value)](#setTextBoxWrapMode-int) | يحدد كيفية التفاف النص داخل الشكل. |
| [setVerticalAnchor(int value)](#setVerticalAnchor-int) | يحدد محاذاة النص العمودية داخل الشكل. |
### breakForwardLink() {#breakForwardLink}
```
public void breakForwardLink()
```


يفصل الرابط إلى الـ [TextBox](../../com.aspose.words/textbox/) التالي.

 **Remarks:** 

[breakForwardLink()](../../com.aspose.words/textbox/\#breakForwardLink) doesn't break all other links in the current sequence of shapes. For example: 1-2-3-4 sequence and [breakForwardLink()](../../com.aspose.words/textbox/\#breakForwardLink) at the 2-nd textbox will create two sequences 1-2, 3-4.

 **Examples:** 

يعرض كيفية ربط صناديق النص.

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


يحدد ما إذا كان Microsoft Word سيزيد حجم الشكل ليتناسب مع النص.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية جعل مربع النص يعيد تحجيم نفسه ليتناسب بإحكام مع محتوياته.

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
boolean - القيمة المنطقية المقابلة.
### getInternalMarginBottom() {#getInternalMarginBottom}
```
public double getInternalMarginBottom()
```


يحدد الهامش الداخلي السفلي بالنقاط لشكل.

 **Remarks:** 

القيمة الافتراضية هي 1/20 بوصة.

 **Examples:** 

يعرض كيفية تعيين الهوامش الداخلية لمربع النص.

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
double - القيمة المقابلة للـ double.
### getInternalMarginLeft() {#getInternalMarginLeft}
```
public double getInternalMarginLeft()
```


يحدد الهامش الداخلي الأيسر بالنقاط لشكل.

 **Remarks:** 

القيمة الافتراضية هي 1/10 بوصة.

 **Examples:** 

يعرض كيفية تعيين الهوامش الداخلية لمربع النص.

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
double - القيمة المقابلة للـ double.
### getInternalMarginRight() {#getInternalMarginRight}
```
public double getInternalMarginRight()
```


يحدد الهامش الداخلي الأيمن بالنقاط لشكل.

 **Remarks:** 

القيمة الافتراضية هي 1/10 بوصة.

 **Examples:** 

يعرض كيفية تعيين الهوامش الداخلية لمربع النص.

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
double - القيمة المقابلة للـ double.
### getInternalMarginTop() {#getInternalMarginTop}
```
public double getInternalMarginTop()
```


يحدد الهامش الداخلي العلوي بالنقاط لشكل.

 **Remarks:** 

القيمة الافتراضية هي 1/20 بوصة.

 **Examples:** 

يعرض كيفية تعيين الهوامش الداخلية لمربع النص.

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
double - القيمة المقابلة للـ double.
### getLayoutFlow() {#getLayoutFlow}
```
public int getLayoutFlow()
```


يحدد تدفق تخطيط النص داخل الشكل.

 **Remarks:** 

القيمة الافتراضية هي [LayoutFlow.HORIZONTAL](../../com.aspose.words/layoutflow/\#HORIZONTAL).

 **Examples:** 

يعرض كيفية تعيين اتجاه النص داخل مربع النص.

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
int - القيمة المقابلة للـ int. القيمة المرتجعة هي إحدى ثوابت [LayoutFlow](../../com.aspose.words/layoutflow/).
### getNext() {#getNext}
```
public TextBox getNext()
```


يحصل على [TextBox](../../com.aspose.words/textbox/) الذي يمثل الـ [TextBox](../../com.aspose.words/textbox/) التالي في تسلسل الأشكال.

 **Examples:** 

يعرض كيفية ربط صناديق النص.

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


يحصل على قيمة منطقية تشير إلى ما إذا كان نص الـ TextBox يجب ألا يدور عندما يتم تدوير الشكل.

 **Remarks:** 

القيمة الافتراضية هي false

 **Examples:** 

يوضح كيفية تعطيل دوران النص عندما يتم تدوير الشكل.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.ELLIPSE, 20.0, 20.0);
 shape.getTextBox().setNoTextRotation(true);

 doc.save(getArtifactsDir() + "Shape.NoTextRotation.docx");
 
```

**Returns:**
boolean - قيمة منطقية تشير إلى أن نص الـ TextBox يجب ألا يدور عندما يتم تدوير الشكل.
### getParent() {#getParent}
```
public Shape getParent()
```


يحصل على الشكل الأب للـ [TextBox](../../com.aspose.words/textbox/).

**Returns:**
[Shape](../../com.aspose.words/shape/) - A parent shape for the [TextBox](../../com.aspose.words/textbox/).
### getPrevious() {#getPrevious}
```
public TextBox getPrevious()
```


يعيد [TextBox](../../com.aspose.words/textbox/) الذي يمثل الـ [TextBox](../../com.aspose.words/textbox/) السابق في تسلسل الأشكال.

 **Examples:** 

يعرض كيفية ربط صناديق النص.

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


يحدد كيفية التفاف النص داخل الشكل.

 **Remarks:** 

القيمة الافتراضية هي [TextBoxWrapMode.SQUARE](../../com.aspose.words/textboxwrapmode/\#SQUARE).

 **Examples:** 

يوضح كيفية تعيين وضع الالتفاف لمحتويات مربع النص.

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
int - القيمة المقابلة للـ int. القيمة المرتجعة هي إحدى ثوابت [TextBoxWrapMode](../../com.aspose.words/textboxwrapmode/).
### getVerticalAnchor() {#getVerticalAnchor}
```
public int getVerticalAnchor()
```


يحدد محاذاة النص العمودية داخل الشكل.

 **Remarks:** 

القيمة الافتراضية هي [TextBoxAnchor.TOP](../../com.aspose.words/textboxanchor/\#TOP).

 **Examples:** 

يوضح كيفية محاذاة محتوى النص عموديًا داخل مربع النص.

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
int - القيمة المقابلة للـ int. القيمة المرتجعة هي إحدى ثوابت [TextBoxAnchor](../../com.aspose.words/textboxanchor/).
### isValidLinkTarget(TextBox target) {#isValidLinkTarget-com.aspose.words.TextBox}
```
public boolean isValidLinkTarget(TextBox target)
```


يحدد ما إذا كان يمكن ربط هذا الـ [TextBox](../../com.aspose.words/textbox/) بـ [TextBox](../../com.aspose.words/textbox/) الهدف.

 **Examples:** 

يعرض كيفية ربط صناديق النص.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| target | [TextBox](../../com.aspose.words/textbox/) |  |

**Returns:**
boolean
### setFitShapeToText(boolean value) {#setFitShapeToText-boolean}
```
public void setFitShapeToText(boolean value)
```


يحدد ما إذا كان Microsoft Word سيزيد حجم الشكل ليتناسب مع النص.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يعرض كيفية جعل مربع النص يعيد تحجيم نفسه ليتناسب بإحكام مع محتوياته.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setInternalMarginBottom(double value) {#setInternalMarginBottom-double}
```
public void setInternalMarginBottom(double value)
```


يحدد الهامش الداخلي السفلي بالنقاط لشكل.

 **Remarks:** 

القيمة الافتراضية هي 1/20 بوصة.

 **Examples:** 

يعرض كيفية تعيين الهوامش الداخلية لمربع النص.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | القيمة العشرية المقابلة. |

### setInternalMarginLeft(double value) {#setInternalMarginLeft-double}
```
public void setInternalMarginLeft(double value)
```


يحدد الهامش الداخلي الأيسر بالنقاط لشكل.

 **Remarks:** 

القيمة الافتراضية هي 1/10 بوصة.

 **Examples:** 

يعرض كيفية تعيين الهوامش الداخلية لمربع النص.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | القيمة العشرية المقابلة. |

### setInternalMarginRight(double value) {#setInternalMarginRight-double}
```
public void setInternalMarginRight(double value)
```


يحدد الهامش الداخلي الأيمن بالنقاط لشكل.

 **Remarks:** 

القيمة الافتراضية هي 1/10 بوصة.

 **Examples:** 

يعرض كيفية تعيين الهوامش الداخلية لمربع النص.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | القيمة العشرية المقابلة. |

### setInternalMarginTop(double value) {#setInternalMarginTop-double}
```
public void setInternalMarginTop(double value)
```


يحدد الهامش الداخلي العلوي بالنقاط لشكل.

 **Remarks:** 

القيمة الافتراضية هي 1/20 بوصة.

 **Examples:** 

يعرض كيفية تعيين الهوامش الداخلية لمربع النص.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | القيمة العشرية المقابلة. |

### setLayoutFlow(int value) {#setLayoutFlow-int}
```
public void setLayoutFlow(int value)
```


يحدد تدفق تخطيط النص داخل الشكل.

 **Remarks:** 

القيمة الافتراضية هي [LayoutFlow.HORIZONTAL](../../com.aspose.words/layoutflow/\#HORIZONTAL).

 **Examples:** 

يعرض كيفية تعيين اتجاه النص داخل مربع النص.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | القيمة المقابلة للـ int. يجب أن تكون القيمة إحدى ثوابت [LayoutFlow](../../com.aspose.words/layoutflow/). |

### setNext(TextBox value) {#setNext-com.aspose.words.TextBox}
```
public void setNext(TextBox value)
```


يضبط [TextBox](../../com.aspose.words/textbox/) الذي يمثل الـ [TextBox](../../com.aspose.words/textbox/) التالي في تسلسل الأشكال.

 **Examples:** 

يعرض كيفية ربط صناديق النص.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [TextBox](../../com.aspose.words/textbox/) | [TextBox](../../com.aspose.words/textbox/) يمثل الـ [TextBox](../../com.aspose.words/textbox/) التالي في تسلسل الأشكال. |

### setNoTextRotation(boolean value) {#setNoTextRotation-boolean}
```
public void setNoTextRotation(boolean value)
```


يضبط قيمة منطقية تشير إلى ما إذا كان نص الـ TextBox يجب ألا يدور عندما يتم تدوير الشكل.

 **Remarks:** 

القيمة الافتراضية هي false

 **Examples:** 

يوضح كيفية تعطيل دوران النص عندما يتم تدوير الشكل.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.ELLIPSE, 20.0, 20.0);
 shape.getTextBox().setNoTextRotation(true);

 doc.save(getArtifactsDir() + "Shape.NoTextRotation.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | قيمة منطقية تشير إلى أن نص الـ TextBox يجب ألا يدور عندما يتم تدوير الشكل. |

### setTextBoxWrapMode(int value) {#setTextBoxWrapMode-int}
```
public void setTextBoxWrapMode(int value)
```


يحدد كيفية التفاف النص داخل الشكل.

 **Remarks:** 

القيمة الافتراضية هي [TextBoxWrapMode.SQUARE](../../com.aspose.words/textboxwrapmode/\#SQUARE).

 **Examples:** 

يوضح كيفية تعيين وضع الالتفاف لمحتويات مربع النص.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | القيمة المقابلة للـ int. يجب أن تكون القيمة إحدى ثوابت [TextBoxWrapMode](../../com.aspose.words/textboxwrapmode/). |

### setVerticalAnchor(int value) {#setVerticalAnchor-int}
```
public void setVerticalAnchor(int value)
```


يحدد محاذاة النص العمودية داخل الشكل.

 **Remarks:** 

القيمة الافتراضية هي [TextBoxAnchor.TOP](../../com.aspose.words/textboxanchor/\#TOP).

 **Examples:** 

يوضح كيفية محاذاة محتوى النص عموديًا داخل مربع النص.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | القيمة المقابلة للـ int. يجب أن تكون القيمة إحدى ثوابت [TextBoxAnchor](../../com.aspose.words/textboxanchor/). |

