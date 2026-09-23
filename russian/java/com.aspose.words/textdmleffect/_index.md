---
title: "TextDmlEffect"
linktitle: "TextDmlEffect"
second_title: "Aspose.Words для Java"
description: "Эффект Dml текста для текстовых фрагментов в Java."
type: docs
weight: 672
url: /ru/java/com.aspose.words/textdmleffect/
---

**Inheritance:**
java.lang.Object
```
public class TextDmlEffect
```

Эффект DML текста для последовательностей текста.

 **Examples:** 

Показывает, как проверить, отображает ли фрагмент эффект текста DrawingML.

```

 Document doc = new Document(getMyDir() + "DrawingML text effects.docx");

 RunCollection runs = doc.getFirstSection().getBody().getFirstParagraph().getRuns();

 Assert.assertTrue(runs.get(0).getFont().hasDmlEffect(TextDmlEffect.SHADOW));
 Assert.assertTrue(runs.get(1).getFont().hasDmlEffect(TextDmlEffect.SHADOW));
 Assert.assertTrue(runs.get(2).getFont().hasDmlEffect(TextDmlEffect.REFLECTION));
 Assert.assertTrue(runs.get(3).getFont().hasDmlEffect(TextDmlEffect.EFFECT_3_D));
 Assert.assertTrue(runs.get(4).getFont().hasDmlEffect(TextDmlEffect.FILL));
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [EFFECT_3_D](#EFFECT-3-D) | 3D-эффект. |
| [FILL](#FILL) | Эффект наложения заполнения. |
| [GLOW](#GLOW) | Эффект свечения, при котором цветная размазанная обводка добавляется за пределами краёв объекта. |
| [OUTLINE](#OUTLINE) | Эффект контура. |
| [REFLECTION](#REFLECTION) | Эффект отражения. |
| [SHADOW](#SHADOW) | Эффект тени. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String textDmlEffectName)](#fromName-java.lang.String) |  |
| [getName(int textDmlEffect)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textDmlEffect)](#toString-int) |  |
### EFFECT_3_D {#EFFECT-3-D}
```
public static int EFFECT_3_D
```


3D-эффект.

### FILL {#FILL}
```
public static int FILL
```


Эффект наложения заполнения.

### GLOW {#GLOW}
```
public static int GLOW
```


Эффект свечения, при котором цветная размазанная обводка добавляется за пределами краёв объекта.

### OUTLINE {#OUTLINE}
```
public static int OUTLINE
```


Эффект контура.

### REFLECTION {#REFLECTION}
```
public static int REFLECTION
```


Эффект отражения.

### SHADOW {#SHADOW}
```
public static int SHADOW
```


Эффект тени.

### length {#length}
```
public static int length
```


### fromName(String textDmlEffectName) {#fromName-java.lang.String}
```
public static int fromName(String textDmlEffectName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| textDmlEffectName | java.lang.String |  |

**Returns:**
int
### getName(int textDmlEffect) {#getName-int}
```
public static String getName(int textDmlEffect)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| textDmlEffect | int |  |

**Returns:**
java.lang.String
