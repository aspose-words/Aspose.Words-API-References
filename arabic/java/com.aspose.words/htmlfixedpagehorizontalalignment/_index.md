---
title: "HtmlFixedPageHorizontalAlignment"
linktitle: "HtmlFixedPageHorizontalAlignment"
second_title: "Aspose.Words لـ Java"
description: "يحدد المحاذاة الأفقية للصفحات في مستند HTML الناتج في جافا."
type: docs
weight: 379
url: /ar/java/com.aspose.words/htmlfixedpagehorizontalalignment/
---

**Inheritance:**
java.lang.Object
```
public class HtmlFixedPageHorizontalAlignment
```

يحدد المحاذاة الأفقية للصفحات في مستند HTML الناتج.

 **Examples:** 

يعرض كيفية تعيين محاذاة الصفحات أفقياً عند حفظ مستند إلى HTML.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();
 {
     htmlFixedSaveOptions.setPageHorizontalAlignment(pageHorizontalAlignment);
 }

 doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.HorizontalAlignment.html", htmlFixedSaveOptions);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlFixedSaveOptions.HorizontalAlignment/styles.css"), StandardCharsets.UTF_8);

 switch (pageHorizontalAlignment)
 {
     case HtmlFixedPageHorizontalAlignment.CENTER:
         Assert.assertTrue(Pattern.compile(
             "[.]awpage [{] position:relative; border:solid 1pt black; margin:10pt auto 10pt auto; overflow:hidden; [}]").matcher(outDocContents).find());
         break;
     case HtmlFixedPageHorizontalAlignment.LEFT:
         Assert.assertTrue(Pattern.compile(
             "[.]awpage [{] position:relative; border:solid 1pt black; margin:10pt auto 10pt 10pt; overflow:hidden; [}]").matcher(outDocContents).find());
         break;
     case HtmlFixedPageHorizontalAlignment.RIGHT:
         Assert.assertTrue(Pattern.compile(
             "[.]awpage [{] position:relative; border:solid 1pt black; margin:10pt 10pt 10pt auto; overflow:hidden; [}]").matcher(outDocContents).find());
         break;
 }
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [CENTER](#CENTER) | توسيط الصفحات. |
| [LEFT](#LEFT) | محاذاة الصفحات إلى اليسار. |
| [RIGHT](#RIGHT) | محاذاة الصفحات إلى اليمين. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String htmlFixedPageHorizontalAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int htmlFixedPageHorizontalAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int htmlFixedPageHorizontalAlignment)](#toString-int) |  |
### CENTER {#CENTER}
```
public static int CENTER
```


توسيط الصفحات. هذه هي القيمة الافتراضية.

### LEFT {#LEFT}
```
public static int LEFT
```


محاذاة الصفحات إلى اليسار.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


محاذاة الصفحات إلى اليمين.

### length {#length}
```
public static int length
```


### fromName(String htmlFixedPageHorizontalAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String htmlFixedPageHorizontalAlignmentName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| htmlFixedPageHorizontalAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int htmlFixedPageHorizontalAlignment) {#getName-int}
```
public static String getName(int htmlFixedPageHorizontalAlignment)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| htmlFixedPageHorizontalAlignment | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int htmlFixedPageHorizontalAlignment) {#toString-int}
```
public static String toString(int htmlFixedPageHorizontalAlignment)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| htmlFixedPageHorizontalAlignment | int |  |

**Returns:**
java.lang.String
