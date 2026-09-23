---
title: "TextDmlEffect"
linktitle: "TextDmlEffect"
second_title: "Aspose.Words per Java"
description: "Effetto testo Dml per le sequenze di testo in Java."
type: docs
weight: 672
url: /it/java/com.aspose.words/textdmleffect/
---

**Inheritance:**
java.lang.Object
```
public class TextDmlEffect
```

Effetto di testo Dml per le sequenze di testo.

 **Examples:** 

Mostra come verificare se una sequenza visualizza un effetto testo DrawingML.

```

 Document doc = new Document(getMyDir() + "DrawingML text effects.docx");

 RunCollection runs = doc.getFirstSection().getBody().getFirstParagraph().getRuns();

 Assert.assertTrue(runs.get(0).getFont().hasDmlEffect(TextDmlEffect.SHADOW));
 Assert.assertTrue(runs.get(1).getFont().hasDmlEffect(TextDmlEffect.SHADOW));
 Assert.assertTrue(runs.get(2).getFont().hasDmlEffect(TextDmlEffect.REFLECTION));
 Assert.assertTrue(runs.get(3).getFont().hasDmlEffect(TextDmlEffect.EFFECT_3_D));
 Assert.assertTrue(runs.get(4).getFont().hasDmlEffect(TextDmlEffect.FILL));
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [EFFECT_3_D](#EFFECT-3-D) | Effetto 3D. |
| [FILL](#FILL) | Effetto di sovrapposizione di riempimento. |
| [GLOW](#GLOW) | Effetto bagliore, in cui un contorno sfocato colorato viene aggiunto al di fuori dei bordi dell'oggetto. |
| [OUTLINE](#OUTLINE) | Effetto contorno. |
| [REFLECTION](#REFLECTION) | Effetto riflessione. |
| [SHADOW](#SHADOW) | Effetto ombra. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String textDmlEffectName)](#fromName-java.lang.String) |  |
| [getName(int textDmlEffect)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textDmlEffect)](#toString-int) |  |
### EFFECT_3_D {#EFFECT-3-D}
```
public static int EFFECT_3_D
```


Effetto 3D.

### FILL {#FILL}
```
public static int FILL
```


Effetto di sovrapposizione di riempimento.

### GLOW {#GLOW}
```
public static int GLOW
```


Effetto bagliore, in cui un contorno sfocato colorato viene aggiunto al di fuori dei bordi dell'oggetto.

### OUTLINE {#OUTLINE}
```
public static int OUTLINE
```


Effetto contorno.

### REFLECTION {#REFLECTION}
```
public static int REFLECTION
```


Effetto riflessione.

### SHADOW {#SHADOW}
```
public static int SHADOW
```


Effetto ombra.

### length {#length}
```
public static int length
```


### fromName(String textDmlEffectName) {#fromName-java.lang.String}
```
public static int fromName(String textDmlEffectName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| textDmlEffectName | java.lang.String |  |

**Returns:**
int
### getName(int textDmlEffect) {#getName-int}
```
public static String getName(int textDmlEffect)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| textDmlEffect | int |  |

**Returns:**
java.lang.String
