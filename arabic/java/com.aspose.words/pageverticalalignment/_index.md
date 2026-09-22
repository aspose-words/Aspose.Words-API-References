---
title: "PageVerticalAlignment"
linktitle: "PageVerticalAlignment"
second_title: "Aspose.Words لـ Java"
description: "يحدد محاذاة النص عموديًا على كل صفحة في Java."
type: docs
weight: 520
url: /ar/java/com.aspose.words/pageverticalalignment/
---

**Inheritance:**
java.lang.Object
```
public class PageVerticalAlignment
```

يحدد محاذاة النص العمودية على كل صفحة.

 **Examples:** 

يوضح كيفية تطبيق وإرجاع إعدادات إعداد الصفحة للأقسام في المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [BOTTOM](#BOTTOM) | النص مُحاذى في أسفل الصفحة. |
| [CENTER](#CENTER) | النص مُحاذى في وسط الصفحة. |
| [JUSTIFY](#JUSTIFY) | النص مُمتد لملء الصفحة. |
| [TOP](#TOP) | النص مُحاذى في أعلى الصفحة. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String pageVerticalAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int pageVerticalAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pageVerticalAlignment)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


النص مُحاذى في أسفل الصفحة.

### CENTER {#CENTER}
```
public static int CENTER
```


النص مُحاذى في وسط الصفحة.

### JUSTIFY {#JUSTIFY}
```
public static int JUSTIFY
```


النص مُمتد لملء الصفحة.

### TOP {#TOP}
```
public static int TOP
```


النص مُحاذى في أعلى الصفحة.

### length {#length}
```
public static int length
```


### fromName(String pageVerticalAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String pageVerticalAlignmentName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| pageVerticalAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int pageVerticalAlignment) {#getName-int}
```
public static String getName(int pageVerticalAlignment)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| pageVerticalAlignment | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pageVerticalAlignment) {#toString-int}
```
public static String toString(int pageVerticalAlignment)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| pageVerticalAlignment | int |  |

**Returns:**
java.lang.String
