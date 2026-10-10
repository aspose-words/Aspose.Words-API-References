---
title: "TextDmlEffect"
linktitle: "TextDmlEffect"
second_title: "Aspose.Words لـ Java"
description: "تأثير نص Dml لتشغيلات النص في Java."
type: docs
weight: 672
url: /ar/java/com.aspose.words/textdmleffect/
---

**Inheritance:**
java.lang.Object
```
public class TextDmlEffect
```

تأثير نص Dml لتشغيلات النص.

 **Examples:** 

يوضح كيفية التحقق مما إذا كانت تشغيلية تعرض تأثير نص DrawingML.

```

 Document doc = new Document(getMyDir() + "DrawingML text effects.docx");

 RunCollection runs = doc.getFirstSection().getBody().getFirstParagraph().getRuns();

 Assert.assertTrue(runs.get(0).getFont().hasDmlEffect(TextDmlEffect.SHADOW));
 Assert.assertTrue(runs.get(1).getFont().hasDmlEffect(TextDmlEffect.SHADOW));
 Assert.assertTrue(runs.get(2).getFont().hasDmlEffect(TextDmlEffect.REFLECTION));
 Assert.assertTrue(runs.get(3).getFont().hasDmlEffect(TextDmlEffect.EFFECT_3_D));
 Assert.assertTrue(runs.get(4).getFont().hasDmlEffect(TextDmlEffect.FILL));
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [EFFECT_3_D](#EFFECT-3-D) | تأثير ثلاثي الأبعاد. |
| [FILL](#FILL) | تأثير تعبئة التراكب. |
| [GLOW](#GLOW) | تأثير التوهج، حيث يتم إضافة حد ملون ضبابي خارج حواف الكائن. |
| [OUTLINE](#OUTLINE) | تأثير الخط الخارجي. |
| [REFLECTION](#REFLECTION) | تأثير الانعكاس. |
| [SHADOW](#SHADOW) | تأثير الظل. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String textDmlEffectName)](#fromName-java.lang.String) |  |
| [getName(int textDmlEffect)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textDmlEffect)](#toString-int) |  |
### EFFECT_3_D {#EFFECT-3-D}
```
public static int EFFECT_3_D
```


تأثير ثلاثي الأبعاد.

### FILL {#FILL}
```
public static int FILL
```


تأثير تعبئة التراكب.

### GLOW {#GLOW}
```
public static int GLOW
```


تأثير التوهج، حيث يتم إضافة حد ملون ضبابي خارج حواف الكائن.

### OUTLINE {#OUTLINE}
```
public static int OUTLINE
```


تأثير الخط الخارجي.

### REFLECTION {#REFLECTION}
```
public static int REFLECTION
```


تأثير الانعكاس.

### SHADOW {#SHADOW}
```
public static int SHADOW
```


تأثير الظل.

### length {#length}
```
public static int length
```


### fromName(String textDmlEffectName) {#fromName-java.lang.String}
```
public static int fromName(String textDmlEffectName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| textDmlEffectName | java.lang.String |  |

**Returns:**
int
### getName(int textDmlEffect) {#getName-int}
```
public static String getName(int textDmlEffect)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| textDmlEffect | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int textDmlEffect) {#toString-int}
```
public static String toString(int textDmlEffect)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| textDmlEffect | int |  |

**Returns:**
java.lang.String
