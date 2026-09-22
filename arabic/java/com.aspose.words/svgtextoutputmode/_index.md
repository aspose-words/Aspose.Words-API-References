---
title: "SvgTextOutputMode"
linktitle: "SvgTextOutputMode"
second_title: "Aspose.Words لـ Java"
description: "يسمح بتحديد كيفية عرض النص داخل المستند عند الحفظ بتنسيق SVG في Java."
type: docs
weight: 650
url: /ar/java/com.aspose.words/svgtextoutputmode/
---

**Inheritance:**
java.lang.Object
```
public class SvgTextOutputMode
```

يسمح بتحديد كيفية عرض النص داخل المستند عند الحفظ بتنسيق SVG.

 **Examples:** 

يعرض كيفية محاكاة خصائص الصور عند تحويل مستند .docx إلى .svg.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 // Configure the SvgSaveOptions object to save with no page borders or selectable text.
 SvgSaveOptions options = new SvgSaveOptions();
 {
     options.setFitToViewPort(true);
     options.setShowPageBorder(false);
     options.setTextOutputMode(SvgTextOutputMode.USE_PLACED_GLYPHS);
 }

 doc.save(getArtifactsDir() + "SvgSaveOptions.SaveLikeImage.svg", options);
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [USE_PLACED_GLYPHS](#USE-PLACED-GLYPHS) | يتم عرض النص باستخدام المنحنيات. |
| [USE_SVG_FONTS](#USE-SVG-FONTS) | يتم استخدام خطوط SVG لعرض النص. |
| [USE_TARGET_MACHINE_FONTS](#USE-TARGET-MACHINE-FONTS) | يتم استخدام الخطوط المثبتة على الجهاز الهدف لعرض النص. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String svgTextOutputModeName)](#fromName-java.lang.String) |  |
| [getName(int svgTextOutputMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int svgTextOutputMode)](#toString-int) |  |
### USE_PLACED_GLYPHS {#USE-PLACED-GLYPHS}
```
public static int USE_PLACED_GLYPHS
```


يتم عرض النص باستخدام المنحنيات. ملاحظة، لن يعمل تحديد النص إذا استخدمت هذا الخيار.

### USE_SVG_FONTS {#USE-SVG-FONTS}
```
public static int USE_SVG_FONTS
```


يتم استخدام خطوط SVG لعرض النص. ملاحظة، لا تدعم جميع المتصفحات خطوط SVG.

### USE_TARGET_MACHINE_FONTS {#USE-TARGET-MACHINE-FONTS}
```
public static int USE_TARGET_MACHINE_FONTS
```


يتم استخدام الخطوط المثبتة على الجهاز الهدف لعرض النص. ملاحظة، إذا لم تتوفر بعض الخطوط المستخدمة في المستند على الجهاز الهدف، قد يظهر المستند بشكل مختلف.

### length {#length}
```
public static int length
```


### fromName(String svgTextOutputModeName) {#fromName-java.lang.String}
```
public static int fromName(String svgTextOutputModeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| svgTextOutputModeName | java.lang.String |  |

**Returns:**
int
### getName(int svgTextOutputMode) {#getName-int}
```
public static String getName(int svgTextOutputMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| svgTextOutputMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int svgTextOutputMode) {#toString-int}
```
public static String toString(int svgTextOutputMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| svgTextOutputMode | int |  |

**Returns:**
java.lang.String
