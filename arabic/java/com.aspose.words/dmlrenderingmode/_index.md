---
title: "DmlRenderingMode"
linktitle: "DmlRenderingMode"
second_title: "Aspose.Words لـ Java"
description: "يحدد كيفية تحويل أشكال DrawingML إلى صيغ صفحات ثابتة في Java."
type: docs
weight: 158
url: /ar/java/com.aspose.words/dmlrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class DmlRenderingMode
```

يحدد كيفية عرض أشكال DrawingML إلى صيغ الصفحات الثابتة.

 **Examples:** 

يوضح كيفية تكوين جودة عرض تأثيرات DrawingML في مستند عند حفظه كملف PDF.

```

 Document doc = new Document(getMyDir() + "DrawingML shape effects.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.None" to discard all DrawingML effects.
 // Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.Simplified"
 // to render a simplified version of DrawingML effects.
 // Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.Fine" to
 // render DrawingML effects with more accuracy and also with more processing cost.
 options.setDmlEffectsRenderingMode(effectsRenderingMode);

 Assert.assertEquals(DmlRenderingMode.DRAWING_ML, options.getDmlRenderingMode());

 doc.save(getArtifactsDir() + "PdfSaveOptions.DrawingMLEffects.pdf", options);
 
```

يوضح كيفية عرض الأشكال الاحتياطية عند الحفظ كملف PDF.

```

 Document doc = new Document(getMyDir() + "DrawingML shape fallbacks.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "DmlRenderingMode" property to "DmlRenderingMode.Fallback"
 // to substitute DML shapes with their fallback shapes.
 // Set the "DmlRenderingMode" property to "DmlRenderingMode.DrawingML"
 // to render the DML shapes themselves.
 options.setDmlRenderingMode(dmlRenderingMode);

 doc.save(getArtifactsDir() + "PdfSaveOptions.DrawingMLFallback.pdf", options);
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [DRAWING_ML](#DRAWING-ML) | يتجاهل Aspose.Words الشكل الاحتياطي لـ DrawingML ويعرض DrawingML نفسه. |
| [FALLBACK](#FALLBACK) | إذا كان الشكل الاحتياطي متاحًا لـ DrawingML، يقوم Aspose.Words بعرض الشكل الاحتياطي بدلاً من DrawingML. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String dmlRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int dmlRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int dmlRenderingMode)](#toString-int) |  |
### DRAWING_ML {#DRAWING-ML}
```
public static int DRAWING_ML
```


يتجاهل Aspose.Words الشكل الاحتياطي لـ DrawingML ويعرض DrawingML نفسه. هذا هو الوضع الافتراضي.

### FALLBACK {#FALLBACK}
```
public static int FALLBACK
```


إذا كان الشكل الاحتياطي متاحًا لـ DrawingML، يقوم Aspose.Words بعرض الشكل الاحتياطي بدلاً من DrawingML.

 **Remarks:** 

يرجى ملاحظة أنه بعد حفظ مستند إلى صيغة صفحة ثابتة باستخدام وضع عرض DML الاحتياطي، يتم استبدال أشكال DML في نموذج مستند AW بشكل دائم بنظيراتها الاحتياطية. نتيجة لذلك، سيؤدي حفظ المستند نفسه مرة أخرى دائمًا إلى استخدام الأشكال الاحتياطية، حتى إذا تم تعيين [DmlRenderingMode](../../com.aspose.words/dmlrenderingmode/) إلى [DRAWING\\_ML](../../com.aspose.words/dmlrenderingmode/\\#DRAWING-ML).

### length {#length}
```
public static int length
```


### fromName(String dmlRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String dmlRenderingModeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| dmlRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int dmlRenderingMode) {#getName-int}
```
public static String getName(int dmlRenderingMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| dmlRenderingMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int dmlRenderingMode) {#toString-int}
```
public static String toString(int dmlRenderingMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| dmlRenderingMode | int |  |

**Returns:**
java.lang.String
