---
title: "MultiPageLayout"
linktitle: "MultiPageLayout"
second_title: "Aspose.Words لـ Java"
description: "يحدد تخطيطًا لتصيير صفحات متعددة في مخرج واحد في Java."
type: docs
weight: 472
url: /ar/java/com.aspose.words/multipagelayout/
---

**Inheritance:**
java.lang.Object
```
public class MultiPageLayout
```

يحدد تخطيطًا لتصيير صفحات متعددة في مخرج واحد.

 **Remarks:** 

استخدم إحدى طرق المصنع الثابتة لإنشاء تكوين التخطيط.

 **Examples:** 

يظهر كيفية حفظ المستند كصورة JPG باستخدام إعدادات تخطيط متعدد الصفحات.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.JPEG);
 // Set up a grid layout with:
 // - 3 columns per row.
 // - 10pts spacing between pages (horizontal and vertical).
 options.setPageLayout(MultiPageLayout.grid(3, 10f, 10f));

 // Alternative layouts:
 // options.PageLayout = MultiPageLayout.Horizontal(10);
 // options.PageLayout = MultiPageLayout.Vertical(10);

 // Customize the background and border.
 options.getPageLayout().setBackColor(Color.lightGray);
 options.getPageLayout().setBorderColor(Color.BLUE);
 options.getPageLayout().setBorderWidth(2f);

 doc.save(getArtifactsDir() + "ImageSaveOptions.GridLayout.jpg", options);
 
```
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getBackColor()](#getBackColor) | يحصل على لون الخلفية للمخرج. |
| [getBorderColor()](#getBorderColor) | يحصل على لون حد الصفحات. |
| [getBorderWidth()](#getBorderWidth) | يحصل على عرض حد الصفحات. |
| [grid(int columns, float horizontalGap, float verticalGap)](#grid-int-float-float) | ينشئ تخطيطًا تُصَيَّر فيه الصفحات من اليسار إلى اليمين، من الأعلى إلى الأسفل، في شبكة بعدد الأعمدة المحدد. |
| [horizontal(float horizontalGap)](#horizontal-float) | ينشئ تخطيطًا تُصَيَّر فيه جميع الصفحات المحددة أفقيًا جنبًا إلى جنب، من اليسار إلى اليمين، في مخرج واحد. |
| [setBackColor(Color value)](#setBackColor-java.awt.Color) | يضبط لون الخلفية للمخرج. |
| [setBorderColor(Color value)](#setBorderColor-java.awt.Color) | يضبط لون حد الصفحات. |
| [setBorderWidth(float value)](#setBorderWidth-float) | يضبط عرض حد الصفحات. |
| [singlePage()](#singlePage) | ينشئ تخطيطًا يصيّر فقط أول صفحة من الصفحات المحددة. |
| [tiffFrames()](#tiffFrames) | ينشئ تخطيطًا تُصَيَّر فيه كل صفحة كإطار منفصل في صورة TIFF متعددة الإطارات. |
| [vertical(float verticalGap)](#vertical-float) | ينشئ تخطيطًا تُصَيَّر فيه جميع الصفحات المحددة عموديًا واحدة تحت الأخرى في مخرج واحد. |
### getBackColor() {#getBackColor}
```
public Color getBackColor()
```


يحصل على لون الخلفية للمخرج. القيمة الافتراضية هي java.awt.Color\#EMPTY.EMPTY.

**Returns:**
java.awt.Color - لون الخلفية للمخرج.
### getBorderColor() {#getBorderColor}
```
public Color getBorderColor()
```


يحصل على لون حد الصفحات. القيمة الافتراضية هي java.awt.Color\#EMPTY.EMPTY.

**Returns:**
java.awt.Color - لون حد الصفحات.
### getBorderWidth() {#getBorderWidth}
```
public float getBorderWidth()
```


يحصل على عرض حدود الصفحة. القيمة الافتراضية هي 0.

**Returns:**
float - عرض حدود الصفحة.
### grid(int columns, float horizontalGap, float verticalGap) {#grid-int-float-float}
```
public static MultiPageLayout grid(int columns, float horizontalGap, float verticalGap)
```


ينشئ تخطيطًا تُصَيَّر فيه الصفحات من اليسار إلى اليمين، من الأعلى إلى الأسفل، في شبكة بعدد الأعمدة المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الأعمدة | int | عدد الأعمدة في التخطيط. يجب أن يكون أكبر من الصفر. |
| الفجوة الأفقية | float | الفجوة الأفقية بين الأعمدة بالنقاط. |
| الفجوة العمودية | float | الفجوة العمودية بين الصفوف بالنقاط. |

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
### horizontal(float horizontalGap) {#horizontal-float}
```
public static MultiPageLayout horizontal(float horizontalGap)
```


ينشئ تخطيطًا تُصَيَّر فيه جميع الصفحات المحددة أفقيًا جنبًا إلى جنب، من اليسار إلى اليمين، في مخرج واحد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الفجوة الأفقية | float | الفجوة الأفقية بين الصفحات بالنقاط. |

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
### setBackColor(Color value) {#setBackColor-java.awt.Color}
```
public void setBackColor(Color value)
```


يضبط لون خلفية الإخراج. القيمة الافتراضية هي java.awt.Color\#EMPTY.EMPTY.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.awt.Color | لون خلفية الإخراج. |

### setBorderColor(Color value) {#setBorderColor-java.awt.Color}
```
public void setBorderColor(Color value)
```


يضبط لون حدود الصفحة. القيمة الافتراضية هي java.awt.Color\#EMPTY.EMPTY.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.awt.Color | لون حدود الصفحة. |

### setBorderWidth(float value) {#setBorderWidth-float}
```
public void setBorderWidth(float value)
```


يضبط عرض حدود الصفحة. القيمة الافتراضية هي 0.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | float | عرض حدود الصفحة. |

### singlePage() {#singlePage}
```
public static MultiPageLayout singlePage()
```


ينشئ تخطيطًا يصيّر فقط أول صفحة من الصفحات المحددة.

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
### tiffFrames() {#tiffFrames}
```
public static MultiPageLayout tiffFrames()
```


ينشئ تخطيطًا حيث يتم عرض كل صفحة كإطار منفصل في صورة TIFF متعددة الإطارات. ينطبق فقط على صيغ صور TIFF.

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
### vertical(float verticalGap) {#vertical-float}
```
public static MultiPageLayout vertical(float verticalGap)
```


ينشئ تخطيطًا تُصَيَّر فيه جميع الصفحات المحددة عموديًا واحدة تحت الأخرى في مخرج واحد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الفجوة العمودية | float | الفجوة العمودية بين الصفحات بالنقاط. |

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
