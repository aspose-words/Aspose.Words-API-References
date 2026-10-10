---
title: "الاتجاه"
linktitle: "الاتجاه"
second_title: "Aspose.Words لـ Java"
description: "يحدد اتجاه الصفحة في Java."
type: docs
weight: 507
url: /ar/java/com.aspose.words/orientation/
---

**Inheritance:**
java.lang.Object
```
public class Orientation
```

يحدد اتجاه الصفحة.

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
| [LANDSCAPE](#LANDSCAPE) | اتجاه الصفحة أفقي (عريض وقصير). |
| [PORTRAIT](#PORTRAIT) | اتجاه الصفحة عمودي (ضيق وطويل). |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String orientationName)](#fromName-java.lang.String) |  |
| [getName(int orientation)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int orientation)](#toString-int) |  |
### LANDSCAPE {#LANDSCAPE}
```
public static int LANDSCAPE
```


اتجاه الصفحة أفقي (عريض وقصير).

### PORTRAIT {#PORTRAIT}
```
public static int PORTRAIT
```


اتجاه الصفحة عمودي (ضيق وطويل).

### length {#length}
```
public static int length
```


### fromName(String orientationName) {#fromName-java.lang.String}
```
public static int fromName(String orientationName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| orientationName | java.lang.String |  |

**Returns:**
int
### getName(int orientation) {#getName-int}
```
public static String getName(int orientation)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| orientation | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int orientation) {#toString-int}
```
public static String toString(int orientation)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| orientation | int |  |

**Returns:**
java.lang.String
