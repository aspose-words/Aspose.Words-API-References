---
title: "ImlRenderingMode"
linktitle: "ImlRenderingMode"
second_title: "Aspose.Words لـ Java"
description: "يحدد كيفية عرض كائنات الحبر InkML إلى تنسيقات الصفحات الثابتة في Java."
type: docs
weight: 399
url: /ar/java/com.aspose.words/imlrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class ImlRenderingMode
```

يحدد كيفية تحويل كائنات الحبر (InkML) إلى تنسيقات صفحات ثابتة.

 **Examples:** 

يعرض كيفية عرض كائن الحبر.

```

 Document doc = new Document(getMyDir() + "Ink object.docx");

 // Set 'ImlRenderingMode.InkML' ignores fall-back shape of ink (InkML) object and renders InkML itself.
 // If the rendering result is unsatisfactory,
 // please use 'ImlRenderingMode.Fallback' to get a result similar to previous versions.
 ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.JPEG);
 {
     saveOptions.setImlRenderingMode(ImlRenderingMode.INK_ML);
 }

 doc.save(getArtifactsDir() + "ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [FALLBACK](#FALLBACK) | إذا كان الشكل الاحتياطي متاحًا لكائن الحبر (InkML)، فإن Aspose.Words يعرض الشكل الاحتياطي بدلاً من InkML. |
| [INK_ML](#INK-ML) | يتجاهل Aspose.Words الشكل الاحتياطي لكائن الحبر (InkML) ويعرض InkML نفسه. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String imlRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int imlRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int imlRenderingMode)](#toString-int) |  |
### FALLBACK {#FALLBACK}
```
public static int FALLBACK
```


إذا كان الشكل الاحتياطي متاحًا لكائن الحبر (InkML)، فإن Aspose.Words يعرض الشكل الاحتياطي بدلاً من InkML.

 **Remarks:** 

يرجى ملاحظة أنه بعد حفظ المستند بتنسيق صفحة ثابت باستخدام وضع العرض الاحتياطي، يتم استبدال كائنات InkML في نموذج مستند AW بشكل دائم بنظيراتها الاحتياطية. نتيجة لذلك، سيؤدي حفظ المستند نفسه مرة أخرى دائمًا إلى استخدام الأشكال الاحتياطية، حتى إذا تم تعيين [ImlRenderingMode](../../com.aspose.words/imlrenderingmode/) إلى [INK\\_ML](../../com.aspose.words/imlrenderingmode/\\#INK-ML).

### INK_ML {#INK-ML}
```
public static int INK_ML
```


يتجاهل Aspose.Words الشكل الاحتياطي لكائن الحبر (InkML) ويعرض InkML نفسه. هذا هو الوضع الافتراضي.

### length {#length}
```
public static int length
```


### fromName(String imlRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String imlRenderingModeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| imlRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int imlRenderingMode) {#getName-int}
```
public static String getName(int imlRenderingMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| imlRenderingMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int imlRenderingMode) {#toString-int}
```
public static String toString(int imlRenderingMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| imlRenderingMode | int |  |

**Returns:**
java.lang.String
