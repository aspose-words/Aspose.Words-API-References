---
title: "Dml3DEffectsRenderingMode"
linktitle: "Dml3DEffectsRenderingMode"
second_title: "Aspose.Words لـ Java"
description: "يحدد كيفية عرض تأثيرات الأشكال ثلاثية الأبعاد في Java."
type: docs
weight: 156
url: /ar/java/com.aspose.words/dml3deffectsrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class Dml3DEffectsRenderingMode
```

يحدد كيفية عرض تأثيرات الشكل ثلاثي الأبعاد.

 **Examples:** 

يعرض كيفية عرض التأثيرات ثلاثية الأبعاد.

```

 Document doc = new Document(getMyDir() + "DrawingML shape 3D effects.docx");

 RenderCallback warningCallback = new RenderCallback();
 doc.setWarningCallback(warningCallback);

 PdfSaveOptions saveOptions = new PdfSaveOptions();
 saveOptions.setDml3DEffectsRenderingMode(Dml3DEffectsRenderingMode.ADVANCED);

 doc.save(getArtifactsDir() + "PdfSaveOptions.Dml3DEffectsRenderingModeTest.pdf", saveOptions);
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [ADVANCED](#ADVANCED) | عرض قائمة موسعة من التأثيرات الخاصة بما في ذلك التأثيرات ثلاثية الأبعاد المتقدمة مثل الحواف، الإضاءة والمواد. |
| [BASIC](#BASIC) | عرض خفيف الوزن ومستقر، يعتمد على المحرك الداخلي، ولكن التأثيرات المتقدمة مثل الإضاءة والمواد وغيرها من التأثيرات الإضافية لا تُعرض عند استخدام هذا الوضع. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String dml3DEffectsRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int dml3DEffectsRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int dml3DEffectsRenderingMode)](#toString-int) |  |
### ADVANCED {#ADVANCED}
```
public static int ADVANCED
```


عرض قائمة موسعة من التأثيرات الخاصة بما في ذلك التأثيرات ثلاثية الأبعاد المتقدمة مثل الحواف، الإضاءة والمواد.

 **Remarks:** 

يستخدم التنفيذ الحالي OpenGL. يرجى التأكد من تثبيت مكتبة OpenGL الإصدار 1.1 أو أعلى على نظامك قبل الاستخدام. لا يزال هذا الوضع قيد التطوير، وقد لا يتم دعم بعض الأشياء، لذا يُنصح باستخدام وضع [BASIC](../../com.aspose.words/dml3deffectsrenderingmode/\#BASIC) إذا لم يكن نتيجة العرض مقبولة. يرجى الاطلاع على الوثائق للتفاصيل.

### BASIC {#BASIC}
```
public static int BASIC
```


عرض خفيف الوزن ومستقر، يعتمد على المحرك الداخلي، ولكن التأثيرات المتقدمة مثل الإضاءة والمواد وغيرها من التأثيرات الإضافية لا تُعرض عند استخدام هذا الوضع. يرجى الاطلاع على الوثائق للتفاصيل.

### length {#length}
```
public static int length
```


### fromName(String dml3DEffectsRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String dml3DEffectsRenderingModeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| dml3DEffectsRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int dml3DEffectsRenderingMode) {#getName-int}
```
public static String getName(int dml3DEffectsRenderingMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| dml3DEffectsRenderingMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int dml3DEffectsRenderingMode) {#toString-int}
```
public static String toString(int dml3DEffectsRenderingMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| dml3DEffectsRenderingMode | int |  |

**Returns:**
java.lang.String
