---
title: "JoinRunsOptions"
linktitle: "JoinRunsOptions"
second_title: "Aspose.Words لـ Java"
description: "يوفر أعلام التكوين لعملية دمج المقاطع في Java."
type: docs
weight: 406
url: /ar/java/com.aspose.words/joinrunsoptions/
---

**Inheritance:**
java.lang.Object
```
public class JoinRunsOptions
```

يوفر أعلام التكوين لعملية دمج المقاطع.

 **Examples:** 

يظهر كيفية دمج المقاطع ذات التنسيق نفسه مع تجاهل السمات الزائدة وغير المهمة.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create runs with identical visible formatting but some internal differences.
 builder.getFont().setName("Arial");
 builder.getFont().setSize(12.0);
 builder.write("Hello ");
 builder.write("world");

 // Verify runs before join.
 Assert.assertEquals(2, doc.getFirstSection().getBody().getFirstParagraph().getRuns().getCount());
 Assert.assertEquals("Hello ", doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).getText());
 Assert.assertEquals("world", doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(1).getText());

 // Configure options to ignore redundant and insignificant attributes during join.
 JoinRunsOptions options = new JoinRunsOptions();
 options.setIgnoreRedundant(true); // Ignore redundant run properties that don't affect appearance.
 options.setIgnoreInsignificant(true); // Ignore insignificant differences like whitespace-only runs.

 // Join runs that have the same visible formatting using the extended options.
 doc.getFirstSection().getBody().getFirstParagraph().joinRunsWithSameFormatting(options);

 // Verify that runs were successfully joined.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getFirstParagraph().getRuns().getCount());
 Assert.assertEquals("Hello world", doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).getText());

 doc.save(getArtifactsDir() + "Paragraph.JoinRunsWithSameFormattingWithOptions.docx");
 
```
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getIgnoreInsignificant()](#getIgnoreInsignificant) | True تشير إلى أن السمات غير المهمة لجميع المقاطع سيتم تجاهلها عند دمج المقاطع ذات التنسيق نفسه. |
| [getIgnoreRedundant()](#getIgnoreRedundant) | True تشير إلى أن السمات الزائدة لجميع المقاطع سيتم تجاهلها عند دمج المقاطع ذات التنسيق نفسه. |
| [getIgnoreSpacing()](#getIgnoreSpacing) | True تشير إلى أن سمات التباعد لجميع المقاطع سيتم تجاهلها عند دمج المقاطع ذات التنسيق نفسه. |
| [setIgnoreInsignificant(boolean value)](#setIgnoreInsignificant-boolean) | True تشير إلى أن السمات غير المهمة لجميع المقاطع سيتم تجاهلها عند دمج المقاطع ذات التنسيق نفسه. |
| [setIgnoreRedundant(boolean value)](#setIgnoreRedundant-boolean) | True تشير إلى أن السمات الزائدة لجميع المقاطع سيتم تجاهلها عند دمج المقاطع ذات التنسيق نفسه. |
| [setIgnoreSpacing(boolean value)](#setIgnoreSpacing-boolean) | True تشير إلى أن سمات التباعد لجميع المقاطع سيتم تجاهلها عند دمج المقاطع ذات التنسيق نفسه. |
### getIgnoreInsignificant() {#getIgnoreInsignificant}
```
public boolean getIgnoreInsignificant()
```


True تشير إلى أن السمات غير المهمة لجميع المقاطع سيتم تجاهلها عند دمج المقاطع ذات التنسيق نفسه.

 **Remarks:** 

السمات غير المهمة هي تلك السمات التي لا تؤثر بشكل ملحوظ على تنسيق مقطع النص مع المحتوى النصي المحدد. القيمة الافتراضية هي False.

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getIgnoreRedundant() {#getIgnoreRedundant}
```
public boolean getIgnoreRedundant()
```


True تشير إلى أن السمات الزائدة لجميع المقاطع سيتم تجاهلها عند دمج المقاطع ذات التنسيق نفسه.

 **Remarks:** 

السمات الزائدة هي تلك السمات التي لا تؤثر على مقطع النص مع المحتوى النصي المحدد. القيمة الافتراضية هي False.

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getIgnoreSpacing() {#getIgnoreSpacing}
```
public boolean getIgnoreSpacing()
```


True تشير إلى أن سمات التباعد لجميع المقاطع سيتم تجاهلها عند دمج المقاطع ذات التنسيق نفسه.

 **Remarks:** 

القيمة الافتراضية هي False.

**Returns:**
boolean - القيمة المنطقية المقابلة.
### setIgnoreInsignificant(boolean value) {#setIgnoreInsignificant-boolean}
```
public void setIgnoreInsignificant(boolean value)
```


True تشير إلى أن السمات غير المهمة لجميع المقاطع سيتم تجاهلها عند دمج المقاطع ذات التنسيق نفسه.

 **Remarks:** 

السمات غير المهمة هي تلك السمات التي لا تؤثر بشكل ملحوظ على تنسيق مقطع النص مع المحتوى النصي المحدد. القيمة الافتراضية هي False.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setIgnoreRedundant(boolean value) {#setIgnoreRedundant-boolean}
```
public void setIgnoreRedundant(boolean value)
```


True تشير إلى أن السمات الزائدة لجميع المقاطع سيتم تجاهلها عند دمج المقاطع ذات التنسيق نفسه.

 **Remarks:** 

السمات الزائدة هي تلك السمات التي لا تؤثر على مقطع النص مع المحتوى النصي المحدد. القيمة الافتراضية هي False.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setIgnoreSpacing(boolean value) {#setIgnoreSpacing-boolean}
```
public void setIgnoreSpacing(boolean value)
```


True تشير إلى أن سمات التباعد لجميع المقاطع سيتم تجاهلها عند دمج المقاطع ذات التنسيق نفسه.

 **Remarks:** 

القيمة الافتراضية هي False.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

