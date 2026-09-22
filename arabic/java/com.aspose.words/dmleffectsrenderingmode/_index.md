---
title: "DmlEffectsRenderingMode"
linktitle: "DmlEffectsRenderingMode"
second_title: "Aspose.Words لـ Java"
description: "يحدد كيفية عرض تأثيرات DrawingML إلى صيغ الصفحات الثابتة في Java."
type: docs
weight: 157
url: /ar/java/com.aspose.words/dmleffectsrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class DmlEffectsRenderingMode
```

يحدد كيفية عرض تأثيرات DrawingML إلى صيغ الصفحات الثابتة.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [FINE](#FINE) | يتم عرض تأثيرات DrawingML في الوضع الدقيق الذي يتضمن معالجة متقدمة. |
| [NONE](#NONE) | لا يتم عرض أي تأثيرات DrawingML. |
| [SIMPLIFIED](#SIMPLIFIED) | تم تبسيط عرض تأثيرات DrawingML. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String dmlEffectsRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int dmlEffectsRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int dmlEffectsRenderingMode)](#toString-int) |  |
### FINE {#FINE}
```
public static int FINE
```


يتم عرض تأثيرات DrawingML في الوضع الدقيق الذي يتضمن معالجة متقدمة. في هذا الوضع، يعطي عرض التأثيرات نتائج أفضل ولكن بتكلفة أداء أعلى مقارنةً بوضع [SIMPLIFIED](../../com.aspose.words/dmleffectsrenderingmode/\#SIMPLIFIED).

### NONE {#NONE}
```
public static int NONE
```


لا يتم عرض أي تأثيرات DrawingML.

### SIMPLIFIED {#SIMPLIFIED}
```
public static int SIMPLIFIED
```


تم تبسيط عرض تأثيرات DrawingML.

### length {#length}
```
public static int length
```


### fromName(String dmlEffectsRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String dmlEffectsRenderingModeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| dmlEffectsRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int dmlEffectsRenderingMode) {#getName-int}
```
public static String getName(int dmlEffectsRenderingMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| dmlEffectsRenderingMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int dmlEffectsRenderingMode) {#toString-int}
```
public static String toString(int dmlEffectsRenderingMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| dmlEffectsRenderingMode | int |  |

**Returns:**
java.lang.String
