---
title: "TextBox"
linktitle: "TextBox"
second_title: "Aspose.Words Java için"
description: "Bir şekil içinde bir metnin Java'da nasıl görüntüleneceğini belirten öznitelikleri tanımlar."
type: docs
weight: 666
url: /tr/java/com.aspose.words/textbox/
---

**Inheritance:**
java.lang.Object
```
public class TextBox
```

Bir şekil içinde metnin nasıl görüntüleneceğini belirten öznitelikleri tanımlar.

Daha fazla bilgi edinmek için [ Working with Shapes ][Working with Shapes] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Bir şeklin metin özelliklerine erişmek için [Shape.getTextBox()](../../com.aspose.words/shape/\#getTextBox) özelliğini kullanın. [TextBox](../../com.aspose.words/textbox/) sınıfının örneklerini doğrudan oluşturmazsınız.

 **Examples:** 

Bir metin kutusunun içindeki metnin yönünü nasıl ayarlayacağınızı gösterir.

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

Bir metin kutusunun içeriğine sıkı bir şekilde sığacak şekilde kendini yeniden boyutlandırmasını nasıl elde edeceğinizi gösterir.

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

Bir metin kutusu için iç kenar boşluklarını nasıl ayarlayacağınızı gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [breakForwardLink()](#breakForwardLink) | Sonraki [TextBox](../../com.aspose.words/textbox/) bağlantısını keser. |
| [getFitShapeToText()](#getFitShapeToText) | Microsoft Word'ün şekli metne sığacak şekilde büyütüp büyütmeyeceğini belirler. |
| [getInternalMarginBottom()](#getInternalMarginBottom) | Bir şekil için iç alt kenar boşluğunu puan cinsinden belirtir. |
| [getInternalMarginLeft()](#getInternalMarginLeft) | Bir şekil için iç sol kenar boşluğunu puan cinsinden belirtir. |
| [getInternalMarginRight()](#getInternalMarginRight) | Bir şekil için iç sağ kenar boşluğunu puan cinsinden belirtir. |
| [getInternalMarginTop()](#getInternalMarginTop) | Bir şekil için iç üst kenar boşluğunu puan cinsinden belirtir. |
| [getLayoutFlow()](#getLayoutFlow) | Bir şekil içindeki metin düzeninin akışını belirler. |
| [getNext()](#getNext) | Şekil dizisinde sonraki [TextBox](../../com.aspose.words/textbox/) temsil eden bir [TextBox](../../com.aspose.words/textbox/) alır. |
| [getNoTextRotation()](#getNoTextRotation) | Şekil döndürüldüğünde TextBox içindeki metnin dönmemesi gerektiğini belirten bir boolean değer alır. |
| [getParent()](#getParent) | [TextBox](../../com.aspose.words/textbox/) için bir üst şekil alır. |
| [getPrevious()](#getPrevious) | Şekil dizisinde önceki [TextBox](../../com.aspose.words/textbox/) temsil eden bir [TextBox](../../com.aspose.words/textbox/) döndürür. |
| [getTextBoxWrapMode()](#getTextBoxWrapMode) | Metnin bir şekil içinde nasıl sarılacağını belirler. |
| [getVerticalAnchor()](#getVerticalAnchor) | Metnin bir şekil içindeki dikey hizalamasını belirtir. |
| [isValidLinkTarget(TextBox target)](#isValidLinkTarget-com.aspose.words.TextBox) | Bu [TextBox](../../com.aspose.words/textbox/) hedef [TextBox](../../com.aspose.words/textbox/) ile bağlanıp bağlanamayacağını belirler. |
| [setFitShapeToText(boolean value)](#setFitShapeToText-boolean) | Microsoft Word'ün şekli metne sığacak şekilde büyütüp büyütmeyeceğini belirler. |
| [setInternalMarginBottom(double value)](#setInternalMarginBottom-double) | Bir şekil için iç alt kenar boşluğunu puan cinsinden belirtir. |
| [setInternalMarginLeft(double value)](#setInternalMarginLeft-double) | Bir şekil için iç sol kenar boşluğunu puan cinsinden belirtir. |
| [setInternalMarginRight(double value)](#setInternalMarginRight-double) | Bir şekil için iç sağ kenar boşluğunu puan cinsinden belirtir. |
| [setInternalMarginTop(double value)](#setInternalMarginTop-double) | Bir şekil için iç üst kenar boşluğunu puan cinsinden belirtir. |
| [setLayoutFlow(int value)](#setLayoutFlow-int) | Bir şekil içindeki metin düzeninin akışını belirler. |
| [setNext(TextBox value)](#setNext-com.aspose.words.TextBox) | Şekil dizisinde sonraki [TextBox](../../com.aspose.words/textbox/) temsil eden bir [TextBox](../../com.aspose.words/textbox/) ayarlar. |
| [setNoTextRotation(boolean value)](#setNoTextRotation-boolean) | Şekil döndürüldüğünde TextBox içindeki metnin dönmemesi gerektiğini gösteren bir boolean değer ayarlar. |
| [setTextBoxWrapMode(int value)](#setTextBoxWrapMode-int) | Metnin bir şekil içinde nasıl sarılacağını belirler. |
| [setVerticalAnchor(int value)](#setVerticalAnchor-int) | Metnin bir şekil içindeki dikey hizalamasını belirtir. |
### breakForwardLink() {#breakForwardLink}
```
public void breakForwardLink()
```


Sonraki [TextBox](../../com.aspose.words/textbox/) bağlantısını keser.

 **Remarks:** 

[breakForwardLink()](../../com.aspose.words/textbox/\#breakForwardLink) doesn't break all other links in the current sequence of shapes. For example: 1-2-3-4 sequence and [breakForwardLink()](../../com.aspose.words/textbox/\#breakForwardLink) at the 2-nd textbox will create two sequences 1-2, 3-4.

 **Examples:** 

Metin kutularını nasıl bağlayacağınızı gösterir.

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


Microsoft Word'ün şekli metne sığacak şekilde büyütüp büyütmeyeceğini belirler.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

Bir metin kutusunun içeriğine sıkı bir şekilde sığacak şekilde kendini yeniden boyutlandırmasını nasıl elde edeceğinizi gösterir.

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
boolean - İlgili  boolean  değeri.
### getInternalMarginBottom() {#getInternalMarginBottom}
```
public double getInternalMarginBottom()
```


Bir şekil için iç alt kenar boşluğunu puan cinsinden belirtir.

 **Remarks:** 

Varsayılan değer 1/20 inçtir.

 **Examples:** 

Bir metin kutusu için iç kenar boşluklarını nasıl ayarlayacağınızı gösterir.

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
double - İlgili  double  değeri.
### getInternalMarginLeft() {#getInternalMarginLeft}
```
public double getInternalMarginLeft()
```


Bir şekil için iç sol kenar boşluğunu puan cinsinden belirtir.

 **Remarks:** 

Varsayılan değer 1/10 inçtir.

 **Examples:** 

Bir metin kutusu için iç kenar boşluklarını nasıl ayarlayacağınızı gösterir.

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
double - İlgili  double  değeri.
### getInternalMarginRight() {#getInternalMarginRight}
```
public double getInternalMarginRight()
```


Bir şekil için iç sağ kenar boşluğunu puan cinsinden belirtir.

 **Remarks:** 

Varsayılan değer 1/10 inçtir.

 **Examples:** 

Bir metin kutusu için iç kenar boşluklarını nasıl ayarlayacağınızı gösterir.

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
double - İlgili  double  değeri.
### getInternalMarginTop() {#getInternalMarginTop}
```
public double getInternalMarginTop()
```


Bir şekil için iç üst kenar boşluğunu puan cinsinden belirtir.

 **Remarks:** 

Varsayılan değer 1/20 inçtir.

 **Examples:** 

Bir metin kutusu için iç kenar boşluklarını nasıl ayarlayacağınızı gösterir.

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
double - İlgili  double  değeri.
### getLayoutFlow() {#getLayoutFlow}
```
public int getLayoutFlow()
```


Bir şekil içindeki metin düzeninin akışını belirler.

 **Remarks:** 

Varsayılan değer [LayoutFlow.HORIZONTAL](../../com.aspose.words/layoutflow/\#HORIZONTAL).

 **Examples:** 

Bir metin kutusunun içindeki metnin yönünü nasıl ayarlayacağınızı gösterir.

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
int - İlgili  int  değeri. Döndürülen değer, [LayoutFlow](../../com.aspose.words/layoutflow/) sabitlerinden biridir.
### getNext() {#getNext}
```
public TextBox getNext()
```


Şekil dizisinde sonraki [TextBox](../../com.aspose.words/textbox/) temsil eden bir [TextBox](../../com.aspose.words/textbox/) alır.

 **Examples:** 

Metin kutularını nasıl bağlayacağınızı gösterir.

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


Şekil döndürüldüğünde TextBox içindeki metnin dönmemesi gerektiğini belirten bir boolean değer alır.

 **Remarks:** 

Varsayılan değer  false

 **Examples:** 

Şekil döndürüldüğünde metin dönüşünün nasıl devre dışı bırakılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.ELLIPSE, 20.0, 20.0);
 shape.getTextBox().setNoTextRotation(true);

 doc.save(getArtifactsDir() + "Shape.NoTextRotation.docx");
 
```

**Returns:**
boolean - Şekil döndürüldüğünde TextBox içindeki metnin dönmemesi gerektiğini belirten bir boolean değeri.
### getParent() {#getParent}
```
public Shape getParent()
```


[TextBox](../../com.aspose.words/textbox/) için bir üst şekil alır.

**Returns:**
[Shape](../../com.aspose.words/shape/) - A parent shape for the [TextBox](../../com.aspose.words/textbox/).
### getPrevious() {#getPrevious}
```
public TextBox getPrevious()
```


Şekil dizisinde önceki [TextBox](../../com.aspose.words/textbox/) temsil eden bir [TextBox](../../com.aspose.words/textbox/) döndürür.

 **Examples:** 

Metin kutularını nasıl bağlayacağınızı gösterir.

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


Metnin bir şekil içinde nasıl sarılacağını belirler.

 **Remarks:** 

Varsayılan değer [TextBoxWrapMode.SQUARE](../../com.aspose.words/textboxwrapmode/\#SQUARE).

 **Examples:** 

Bir metin kutusunun içeriği için sarma modunun nasıl ayarlanacağını gösterir.

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
int - İlgili  int  değeri. Döndürülen değer, [TextBoxWrapMode](../../com.aspose.words/textboxwrapmode/) sabitlerinden biridir.
### getVerticalAnchor() {#getVerticalAnchor}
```
public int getVerticalAnchor()
```


Metnin bir şekil içindeki dikey hizalamasını belirtir.

 **Remarks:** 

Varsayılan değer [TextBoxAnchor.TOP](../../com.aspose.words/textboxanchor/\#TOP).

 **Examples:** 

Bir metin kutusunun metin içeriğini dikey olarak nasıl hizalayacağını gösterir.

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
int - İlgili  int  değeri. Döndürülen değer, [TextBoxAnchor](../../com.aspose.words/textboxanchor/) sabitlerinden biridir.
### isValidLinkTarget(TextBox target) {#isValidLinkTarget-com.aspose.words.TextBox}
```
public boolean isValidLinkTarget(TextBox target)
```


Bu [TextBox](../../com.aspose.words/textbox/) hedef [TextBox](../../com.aspose.words/textbox/) ile bağlanıp bağlanamayacağını belirler.

 **Examples:** 

Metin kutularını nasıl bağlayacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| target | [TextBox](../../com.aspose.words/textbox/) |  |

**Returns:**
boolean
### setFitShapeToText(boolean value) {#setFitShapeToText-boolean}
```
public void setFitShapeToText(boolean value)
```


Microsoft Word'ün şekli metne sığacak şekilde büyütüp büyütmeyeceğini belirler.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

Bir metin kutusunun içeriğine sıkı bir şekilde sığacak şekilde kendini yeniden boyutlandırmasını nasıl elde edeceğinizi gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setInternalMarginBottom(double value) {#setInternalMarginBottom-double}
```
public void setInternalMarginBottom(double value)
```


Bir şekil için iç alt kenar boşluğunu puan cinsinden belirtir.

 **Remarks:** 

Varsayılan değer 1/20 inçtir.

 **Examples:** 

Bir metin kutusu için iç kenar boşluklarını nasıl ayarlayacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | İlgili  double  değeri. |

### setInternalMarginLeft(double value) {#setInternalMarginLeft-double}
```
public void setInternalMarginLeft(double value)
```


Bir şekil için iç sol kenar boşluğunu puan cinsinden belirtir.

 **Remarks:** 

Varsayılan değer 1/10 inçtir.

 **Examples:** 

Bir metin kutusu için iç kenar boşluklarını nasıl ayarlayacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | İlgili  double  değeri. |

### setInternalMarginRight(double value) {#setInternalMarginRight-double}
```
public void setInternalMarginRight(double value)
```


Bir şekil için iç sağ kenar boşluğunu puan cinsinden belirtir.

 **Remarks:** 

Varsayılan değer 1/10 inçtir.

 **Examples:** 

Bir metin kutusu için iç kenar boşluklarını nasıl ayarlayacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | İlgili  double  değeri. |

### setInternalMarginTop(double value) {#setInternalMarginTop-double}
```
public void setInternalMarginTop(double value)
```


Bir şekil için iç üst kenar boşluğunu puan cinsinden belirtir.

 **Remarks:** 

Varsayılan değer 1/20 inçtir.

 **Examples:** 

Bir metin kutusu için iç kenar boşluklarını nasıl ayarlayacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | İlgili  double  değeri. |

### setLayoutFlow(int value) {#setLayoutFlow-int}
```
public void setLayoutFlow(int value)
```


Bir şekil içindeki metin düzeninin akışını belirler.

 **Remarks:** 

Varsayılan değer [LayoutFlow.HORIZONTAL](../../com.aspose.words/layoutflow/\#HORIZONTAL).

 **Examples:** 

Bir metin kutusunun içindeki metnin yönünü nasıl ayarlayacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili  int  değeri. Değer, [LayoutFlow](../../com.aspose.words/layoutflow/) sabitlerinden biri olmalıdır. |

### setNext(TextBox value) {#setNext-com.aspose.words.TextBox}
```
public void setNext(TextBox value)
```


Şekil dizisinde sonraki [TextBox](../../com.aspose.words/textbox/) temsil eden bir [TextBox](../../com.aspose.words/textbox/) ayarlar.

 **Examples:** 

Metin kutularını nasıl bağlayacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | [TextBox](../../com.aspose.words/textbox/) | Şekiller dizisinde sonraki [TextBox](../../com.aspose.words/textbox/) öğesini temsil eden bir [TextBox](../../com.aspose.words/textbox/). |

### setNoTextRotation(boolean value) {#setNoTextRotation-boolean}
```
public void setNoTextRotation(boolean value)
```


Şekil döndürüldüğünde TextBox içindeki metnin dönmemesi gerektiğini gösteren bir boolean değer ayarlar.

 **Remarks:** 

Varsayılan değer  false

 **Examples:** 

Şekil döndürüldüğünde metin dönüşünün nasıl devre dışı bırakılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.ELLIPSE, 20.0, 20.0);
 shape.getTextBox().setNoTextRotation(true);

 doc.save(getArtifactsDir() + "Shape.NoTextRotation.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Şekil döndürüldüğünde TextBox içindeki metnin dönmemesi gerektiğini belirten bir boolean değeri. |

### setTextBoxWrapMode(int value) {#setTextBoxWrapMode-int}
```
public void setTextBoxWrapMode(int value)
```


Metnin bir şekil içinde nasıl sarılacağını belirler.

 **Remarks:** 

Varsayılan değer [TextBoxWrapMode.SQUARE](../../com.aspose.words/textboxwrapmode/\#SQUARE).

 **Examples:** 

Bir metin kutusunun içeriği için sarma modunun nasıl ayarlanacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili  int  değeri. Değer, [TextBoxWrapMode](../../com.aspose.words/textboxwrapmode/) sabitlerinden biri olmalıdır. |

### setVerticalAnchor(int value) {#setVerticalAnchor-int}
```
public void setVerticalAnchor(int value)
```


Metnin bir şekil içindeki dikey hizalamasını belirtir.

 **Remarks:** 

Varsayılan değer [TextBoxAnchor.TOP](../../com.aspose.words/textboxanchor/\#TOP).

 **Examples:** 

Bir metin kutusunun metin içeriğini dikey olarak nasıl hizalayacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili  int  değeri. Değer, [TextBoxAnchor](../../com.aspose.words/textboxanchor/) sabitlerinden biri olmalıdır. |

