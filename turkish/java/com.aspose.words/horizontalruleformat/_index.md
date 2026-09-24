---
title: "HorizontalRuleFormat"
linktitle: "HorizontalRuleFormat"
second_title: "Aspose.Words Java için"
description: "Java'da yatay kural biçimlendirmesini temsil eder."
type: docs
weight: 376
url: /tr/java/com.aspose.words/horizontalruleformat/
---

**Inheritance:**
java.lang.Object
```
public class HorizontalRuleFormat
```

Yatay kural biçimlendirmesini temsil eder.

Daha fazla bilgi edinmek için [ Working with Shapes ][Working with Shapes] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Yatay kural şekli eklemeyi ve biçimlendirmesini özelleştirmeyi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```


[Working with Shapes]: https://docs.aspose.com/words/java/working-with-shapes/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getAlignment()](#getAlignment) | Yatay kuralın hizalamasını alır. |
| [getColor()](#getColor) | Yatay kuralı dolduran fırça rengini alır. |
| [getHeight()](#getHeight) | Yatay kuralın yüksekliğini alır. |
| [getNoShade()](#getNoShade) | Yatay kural için 3B gölgelendirmenin varlığını gösterir. |
| [getWidthPercent()](#getWidthPercent) | Belirtilen yatay kuralın uzunluğunu, pencere genişliğinin yüzdesi olarak alır. |
| [setAlignment(int value)](#setAlignment-int) | Yatay kuralın hizalamasını ayarlar. |
| [setColor(Color value)](#setColor-java.awt.Color) | Yatay kuralı dolduran fırça rengini ayarlar. |
| [setHeight(double value)](#setHeight-double) | Yatay kuralın yüksekliğini ayarlar. |
| [setNoShade(boolean value)](#setNoShade-boolean) | Yatay kural için 3B gölgelendirmenin varlığını gösterir. |
| [setWidthPercent(double value)](#setWidthPercent-double) | Belirtilen yatay kuralın uzunluğunu, pencere genişliğinin yüzdesi olarak ayarlar. |
### getAlignment() {#getAlignment}
```
public int getAlignment()
```


Yatay kuralın hizalamasını alır.

 **Remarks:** 

Varsayılan değer [HorizontalRuleAlignment.LEFT](../../com.aspose.words/horizontalrulealignment/\#LEFT)'dır.

 **Examples:** 

Yatay kural şekli eklemeyi ve biçimlendirmesini özelleştirmeyi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Returns:**
int - Yatay kuralın hizalaması. Döndürülen değer, [HorizontalRuleAlignment](../../com.aspose.words/horizontalrulealignment/) sabitlerinden biridir.
### getColor() {#getColor}
```
public Color getColor()
```


Yatay kuralı dolduran fırça rengini alır.

 **Remarks:** 

Bu, [Fill.getColor()](../../com.aspose.words/fill/\#getColor) / [Fill.setColor(java.awt.Color)](../../com.aspose.words/fill/\#setColor-java.awt.Color) özelliğine bir kısayoldur.

Varsayılan değer java.awt.Color\#getGray().getGray().

 **Examples:** 

Yatay kural şekli eklemeyi ve biçimlendirmesini özelleştirmeyi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Returns:**
java.awt.Color - Yatay kuralı dolduran fırça rengi.
### getHeight() {#getHeight}
```
public double getHeight()
```


Yatay kuralın yüksekliğini alır.

**Returns:**
double - Yatay kuralın yüksekliği.
### getNoShade() {#getNoShade}
```
public boolean getNoShade()
```


Yatay kural için 3B gölgelendirmenin varlığını gösterir. Eğer true ise, yatay kural 3B gölgelendirme olmadan ve katı renk kullanılarak görüntülenir.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

Yatay kural şekli eklemeyi ve biçimlendirmesini özelleştirmeyi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getWidthPercent() {#getWidthPercent}
```
public double getWidthPercent()
```


Belirtilen yatay kuralın uzunluğunu, pencere genişliğinin yüzdesi olarak alır.

**Returns:**
double - Belirtilen yatay kuralın uzunluğunu, pencere genişliğinin yüzdesi olarak ifade eder.
### setAlignment(int value) {#setAlignment-int}
```
public void setAlignment(int value)
```


Yatay kuralın hizalamasını ayarlar.

 **Remarks:** 

Varsayılan değer [HorizontalRuleAlignment.LEFT](../../com.aspose.words/horizontalrulealignment/\#LEFT)'dır.

 **Examples:** 

Yatay kural şekli eklemeyi ve biçimlendirmesini özelleştirmeyi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Yatay kuralın hizalaması. Değer, [HorizontalRuleAlignment](../../com.aspose.words/horizontalrulealignment/) sabitlerinden biri olmalıdır. |

### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Yatay kuralı dolduran fırça rengini ayarlar.

 **Remarks:** 

Bu, [Fill.getColor()](../../com.aspose.words/fill/\#getColor) / [Fill.setColor(java.awt.Color)](../../com.aspose.words/fill/\#setColor-java.awt.Color) özelliğine bir kısayoldur.

Varsayılan değer java.awt.Color\#getGray().getGray().

 **Examples:** 

Yatay kural şekli eklemeyi ve biçimlendirmesini özelleştirmeyi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.awt.Color | Yatay kuralı dolduran fırça rengi. |

### setHeight(double value) {#setHeight-double}
```
public void setHeight(double value)
```


Yatay kuralın yüksekliğini ayarlar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Yatay kuralın yüksekliği. |

### setNoShade(boolean value) {#setNoShade-boolean}
```
public void setNoShade(boolean value)
```


Yatay kural için 3B gölgelendirmenin varlığını gösterir. Eğer true ise, yatay kural 3B gölgelendirme olmadan ve katı renk kullanılarak görüntülenir.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

Yatay kural şekli eklemeyi ve biçimlendirmesini özelleştirmeyi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setWidthPercent(double value) {#setWidthPercent-double}
```
public void setWidthPercent(double value)
```


Belirtilen yatay kuralın uzunluğunu, pencere genişliğinin yüzdesi olarak ayarlar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Belirtilen yatay kuralın uzunluğu, pencere genişliğinin yüzde olarak ifadesi. |

