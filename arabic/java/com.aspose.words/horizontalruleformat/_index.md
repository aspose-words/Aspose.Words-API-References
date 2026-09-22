---
title: "HorizontalRuleFormat"
linktitle: "HorizontalRuleFormat"
second_title: "Aspose.Words لـ Java"
description: "يمثل تنسيق الخط الأفقي في Java."
type: docs
weight: 376
url: /ar/java/com.aspose.words/horizontalruleformat/
---

**Inheritance:**
java.lang.Object
```
public class HorizontalRuleFormat
```

يمثل تنسيق القاعدة الأفقية.

لمزيد من المعلومات، زر مقالة الوثائق [ Working with Shapes ][Working with Shapes].

 **Examples:** 

يظهر كيفية إدراج شكل خط أفقي، وتخصيص تنسيقه.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getAlignment()](#getAlignment) | يحصل على محاذاة الخط الأفقي. |
| [getColor()](#getColor) | يحصل على لون الفرشاة الذي يملأ الخط الأفقي. |
| [getHeight()](#getHeight) | يحصل على ارتفاع الخط الأفقي. |
| [getNoShade()](#getNoShade) | يشير إلى وجود تظليل ثلاثي الأبعاد للخط الأفقي. |
| [getWidthPercent()](#getWidthPercent) | يحصل على طول الخط الأفقي المحدد معبرًا عنه كنسبة مئوية من عرض النافذة. |
| [setAlignment(int value)](#setAlignment-int) | يضبط محاذاة الخط الأفقي. |
| [setColor(Color value)](#setColor-java.awt.Color) | يضبط لون الفرشاة الذي يملأ الخط الأفقي. |
| [setHeight(double value)](#setHeight-double) | يضبط ارتفاع الخط الأفقي. |
| [setNoShade(boolean value)](#setNoShade-boolean) | يشير إلى وجود تظليل ثلاثي الأبعاد للخط الأفقي. |
| [setWidthPercent(double value)](#setWidthPercent-double) | يضبط طول الخط الأفقي المحدد معبرًا عنه كنسبة مئوية من عرض النافذة. |
### getAlignment() {#getAlignment}
```
public int getAlignment()
```


يحصل على محاذاة الخط الأفقي.

 **Remarks:** 

القيمة الافتراضية هي [HorizontalRuleAlignment.LEFT](../../com.aspose.words/horizontalrulealignment/\#LEFT).

 **Examples:** 

يظهر كيفية إدراج شكل خط أفقي، وتخصيص تنسيقه.

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
int - محاذاة الخط الأفقي. القيمة المرجعة هي واحدة من ثوابت [HorizontalRuleAlignment](../../com.aspose.words/horizontalrulealignment/).
### getColor() {#getColor}
```
public Color getColor()
```


يحصل على لون الفرشاة الذي يملأ الخط الأفقي.

 **Remarks:** 

هذا اختصار إلى الخاصية [Fill.getColor()](../../com.aspose.words/fill/\#getColor) / [Fill.setColor(java.awt.Color)](../../com.aspose.words/fill/\#setColor-java.awt.Color).

القيمة الافتراضية هي java.awt.Color\#getGray().getGray().

 **Examples:** 

يظهر كيفية إدراج شكل خط أفقي، وتخصيص تنسيقه.

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
java.awt.Color - لون الفرشاة الذي يملأ الخط الأفقي.
### getHeight() {#getHeight}
```
public double getHeight()
```


يحصل على ارتفاع الخط الأفقي.

**Returns:**
double - ارتفاع الخط الأفقي.
### getNoShade() {#getNoShade}
```
public boolean getNoShade()
```


يشير إلى وجود تظليل ثلاثي الأبعاد للخط الأفقي. إذا  true , فإن الخط الأفقي يكون بدون تظليل ثلاثي الأبعاد ويُستخدم لون صلب.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يظهر كيفية إدراج شكل خط أفقي، وتخصيص تنسيقه.

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
boolean - القيمة المنطقية المقابلة.
### getWidthPercent() {#getWidthPercent}
```
public double getWidthPercent()
```


يحصل على طول الخط الأفقي المحدد معبرًا عنه كنسبة مئوية من عرض النافذة.

**Returns:**
double - طول الخط الأفقي المحدد معبرًا عنه كنسبة مئوية من عرض النافذة.
### setAlignment(int value) {#setAlignment-int}
```
public void setAlignment(int value)
```


يضبط محاذاة الخط الأفقي.

 **Remarks:** 

القيمة الافتراضية هي [HorizontalRuleAlignment.LEFT](../../com.aspose.words/horizontalrulealignment/\#LEFT).

 **Examples:** 

يظهر كيفية إدراج شكل خط أفقي، وتخصيص تنسيقه.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | محاذاة الخط الأفقي. يجب أن تكون القيمة واحدة من ثوابت [HorizontalRuleAlignment](../../com.aspose.words/horizontalrulealignment/). |

### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


يضبط لون الفرشاة الذي يملأ الخط الأفقي.

 **Remarks:** 

هذا اختصار إلى الخاصية [Fill.getColor()](../../com.aspose.words/fill/\#getColor) / [Fill.setColor(java.awt.Color)](../../com.aspose.words/fill/\#setColor-java.awt.Color).

القيمة الافتراضية هي java.awt.Color\#getGray().getGray().

 **Examples:** 

يظهر كيفية إدراج شكل خط أفقي، وتخصيص تنسيقه.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.awt.Color | لون الفرشاة الذي يملأ الخط الأفقي. |

### setHeight(double value) {#setHeight-double}
```
public void setHeight(double value)
```


يضبط ارتفاع الخط الأفقي.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | ارتفاع الخط الأفقي. |

### setNoShade(boolean value) {#setNoShade-boolean}
```
public void setNoShade(boolean value)
```


يشير إلى وجود تظليل ثلاثي الأبعاد للخط الأفقي. إذا  true , فإن الخط الأفقي يكون بدون تظليل ثلاثي الأبعاد ويُستخدم لون صلب.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يظهر كيفية إدراج شكل خط أفقي، وتخصيص تنسيقه.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setWidthPercent(double value) {#setWidthPercent-double}
```
public void setWidthPercent(double value)
```


يضبط طول الخط الأفقي المحدد معبرًا عنه كنسبة مئوية من عرض النافذة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | طول الخط الأفقي المحدد معبرًا عنه كنسبة مئوية من عرض النافذة. |

