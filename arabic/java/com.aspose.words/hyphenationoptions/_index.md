---
title: "HyphenationOptions"
linktitle: "HyphenationOptions"
second_title: "Aspose.Words لـ Java"
description: "يسمح بتكوين خيارات تجزئة الكلمات في المستند في جافا."
type: docs
weight: 388
url: /ar/java/com.aspose.words/hyphenationoptions/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class HyphenationOptions implements Cloneable
```

يسمح بتكوين خيارات تجزئة المستند.

لمزيد من المعلومات، زر مقالة الوثائق [ Working with Hyphenation ][Working with Hyphenation] .

 **Examples:** 

يظهر كيفية تكوين التجزئة التلقائية.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```


[Working with Hyphenation]: https://docs.aspose.com/words/java/working-with-hyphenation/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getAutoHyphenation()](#getAutoHyphenation) | يحصل على القيمة التي تحدد ما إذا كانت التجزئة التلقائية مفعلة للمستند. |
| [getConsecutiveHyphenLimit()](#getConsecutiveHyphenLimit) | يحصل على الحد الأقصى لعدد الأسطر المتتالية التي يمكن أن تنتهي بشرطات. |
| [getHyphenateCaps()](#getHyphenateCaps) | يحصل على القيمة التي تحدد ما إذا كانت الكلمات المكتوبة بأحرف كبيرة بالكامل تُقسم بشرطات. |
| [getHyphenationZone()](#getHyphenationZone) | يحصل على المسافة بوحدة 1/20 من النقطة من الهامش الأيمن التي لا تريد فيها تقسيم الكلمات بشرطات. |
| [setAutoHyphenation(boolean value)](#setAutoHyphenation-boolean) | يضبط القيمة التي تحدد ما إذا كان التجزئة التلقائية مفعلة للمستند. |
| [setConsecutiveHyphenLimit(int value)](#setConsecutiveHyphenLimit-int) | يضبط الحد الأقصى لعدد الأسطر المتتالية التي يمكن أن تنتهي بشرطات. |
| [setHyphenateCaps(boolean value)](#setHyphenateCaps-boolean) | يضبط القيمة التي تحدد ما إذا كانت الكلمات المكتوبة بأحرف كبيرة بالكامل تُقسم بشرطات. |
| [setHyphenationZone(int value)](#setHyphenationZone-int) | يضبط المسافة بوحدة 1/20 من النقطة من الهامش الأيمن التي لا تريد فيها تقسيم الكلمات بشرطات. |
### getAutoHyphenation() {#getAutoHyphenation}
```
public boolean getAutoHyphenation()
```


يحصل على القيمة التي تحدد ما إذا كانت التجزئة التلقائية مفعلة للمستند. القيمة الافتراضية لهذه الخاصية هي false.

 **Examples:** 

يظهر كيفية تكوين التجزئة التلقائية.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Returns:**
منطقي - القيمة التي تحدد ما إذا كانت التجزئة التلقائية مفعلة للمستند.
### getConsecutiveHyphenLimit() {#getConsecutiveHyphenLimit}
```
public int getConsecutiveHyphenLimit()
```


يحصل على الحد الأقصى لعدد الأسطر المتتالية التي يمكن أن تنتهي بشرطات. القيمة الافتراضية لهذه الخاصية هي 0.

 **Remarks:** 

إذا تم ضبط قيمة هذه الخاصية إلى 0، يمكن لأي عدد من الأسطر المتتالية أن ينتهي بشرطات.

الخاصية لا تؤثر عند الحفظ إلى صيغ صفحات ثابتة مثل PDF.

 **Examples:** 

يظهر كيفية تكوين التجزئة التلقائية.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Returns:**
عدد صحيح - الحد الأقصى لعدد الأسطر المتتالية التي يمكن أن تنتهي بشرطات.
### getHyphenateCaps() {#getHyphenateCaps}
```
public boolean getHyphenateCaps()
```


يحصل على القيمة التي تحدد ما إذا كانت الكلمات المكتوبة بأحرف كبيرة بالكامل تُقسم بشرطات. القيمة الافتراضية لهذه الخاصية هي true.

 **Examples:** 

يظهر كيفية تكوين التجزئة التلقائية.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Returns:**
منطقي - القيمة التي تحدد ما إذا كانت الكلمات المكتوبة بأحرف كبيرة بالكامل تُقسم بشرطات.
### getHyphenationZone() {#getHyphenationZone}
```
public int getHyphenationZone()
```


يحصل على المسافة بوحدة 1/20 من النقطة من الهامش الأيمن التي لا تريد فيها تقسيم الكلمات بشرطات. القيمة الافتراضية لهذه الخاصية هي 360 (0.25 بوصة).

 **Examples:** 

يظهر كيفية تكوين التجزئة التلقائية.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Returns:**
عدد صحيح - المسافة بوحدة 1/20 من النقطة من الهامش الأيمن التي لا تريد فيها تقسيم الكلمات بشرطات.
### setAutoHyphenation(boolean value) {#setAutoHyphenation-boolean}
```
public void setAutoHyphenation(boolean value)
```


يضبط القيمة التي تحدد ما إذا كانت التجزئة التلقائية مفعلة للمستند. القيمة الافتراضية لهذه الخاصية هي false.

 **Examples:** 

يظهر كيفية تكوين التجزئة التلقائية.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة التي تحدد ما إذا كانت التجزئة التلقائية مفعلة للمستند. |

### setConsecutiveHyphenLimit(int value) {#setConsecutiveHyphenLimit-int}
```
public void setConsecutiveHyphenLimit(int value)
```


يضبط الحد الأقصى لعدد الأسطر المتتالية التي يمكن أن تنتهي بشرطات. القيمة الافتراضية لهذه الخاصية هي 0.

 **Remarks:** 

إذا تم ضبط قيمة هذه الخاصية إلى 0، يمكن لأي عدد من الأسطر المتتالية أن ينتهي بشرطات.

الخاصية لا تؤثر عند الحفظ إلى صيغ صفحات ثابتة مثل PDF.

 **Examples:** 

يظهر كيفية تكوين التجزئة التلقائية.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | الحد الأقصى لعدد الأسطر المتتالية التي يمكن أن تنتهي بشرطات. |

### setHyphenateCaps(boolean value) {#setHyphenateCaps-boolean}
```
public void setHyphenateCaps(boolean value)
```


يضبط القيمة التي تحدد ما إذا كانت الكلمات المكتوبة بأحرف كبيرة بالكامل تُقسم بشرطات. القيمة الافتراضية لهذه الخاصية هي true.

 **Examples:** 

يظهر كيفية تكوين التجزئة التلقائية.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة التي تحدد ما إذا كانت الكلمات المكتوبة بأحرف كبيرة بالكامل تُقسم بشرطات. |

### setHyphenationZone(int value) {#setHyphenationZone-int}
```
public void setHyphenationZone(int value)
```


يضبط المسافة بوحدة 1/20 من النقطة من الهامش الأيمن التي لا تريد فيها تقسيم الكلمات بشرطات. القيمة الافتراضية لهذه الخاصية هي 360 (0.25 بوصة).

 **Examples:** 

يظهر كيفية تكوين التجزئة التلقائية.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | المسافة بوحدة 1/20 من النقطة من الهامش الأيمن التي لا تريد فيها تقسيم الكلمات بشرطات. |

