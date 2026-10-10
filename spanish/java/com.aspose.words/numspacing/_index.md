---
title: "NumSpacing"
linktitle: "NumSpacing"
second_title: "Aspose.Words para Java"
description: "Especifica los valores posibles en los que el espaciado de números puede mostrarse en Java."
type: docs
weight: 484
url: /es/java/com.aspose.words/numspacing/
---

**Inheritance:**
java.lang.Object
```
public class NumSpacing
```

Especifica los valores posibles en los que se puede mostrar el espaciado de los numerales.

 **Examples:** 

Muestra cómo establecer el tipo de espaciado del número.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // This effect is only supported in newer versions of MS Word.
 doc.getCompatibilityOptions().optimizeFor(MsWordVersion.WORD_2019);

 builder.write("1 ");
 builder.write("This is an example");

 Run run = doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0);
 if (run.getFont().getNumberSpacing() == NumSpacing.DEFAULT)
     run.getFont().setNumberSpacing(NumSpacing.PROPORTIONAL);

 doc.save(getArtifactsDir() + "Fonts.NumberSpacing.docx");
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [DEFAULT](#DEFAULT) | Especifica que los números se muestran en la forma predeterminada de la fuente\u2019s. |
| [PROPORTIONAL](#PROPORTIONAL) | Especifica que las formas de los números diseñadas como espaciado proporcional se muestren si la fuente lo admite. |
| [TABULAR](#TABULAR) | Especifica que las formas de los números diseñadas como tabulares se muestren si la fuente lo admite. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String numSpacingName)](#fromName-java.lang.String) |  |
| [getName(int numSpacing)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int numSpacing)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Especifica que los números se muestran en la forma predeterminada de la fuente\u2019s.

### PROPORTIONAL {#PROPORTIONAL}
```
public static int PROPORTIONAL
```


Especifica que las formas de los números diseñadas como espaciado proporcional se muestren si la fuente lo admite.

### TABULAR {#TABULAR}
```
public static int TABULAR
```


Especifica que las formas de los números diseñadas como tabulares se muestren si la fuente lo admite.

### length {#length}
```
public static int length
```


### fromName(String numSpacingName) {#fromName-java.lang.String}
```
public static int fromName(String numSpacingName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| numSpacingName | java.lang.String |  |

**Returns:**
int
### getName(int numSpacing) {#getName-int}
```
public static String getName(int numSpacing)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| numSpacing | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int numSpacing) {#toString-int}
```
public static String toString(int numSpacing)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| numSpacing | int |  |

**Returns:**
java.lang.String
