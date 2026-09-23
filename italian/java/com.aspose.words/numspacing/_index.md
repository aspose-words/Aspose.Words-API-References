---
title: "NumSpacing"
linktitle: "NumSpacing"
second_title: "Aspose.Words per Java"
description: "Specifica i valori possibili in cui la spaziatura dei numeri può essere visualizzata in Java."
type: docs
weight: 484
url: /it/java/com.aspose.words/numspacing/
---

**Inheritance:**
java.lang.Object
```
public class NumSpacing
```

Specifica i valori possibili in cui la spaziatura numerica può essere visualizzata.

 **Examples:** 

Mostra come impostare il tipo di spaziatura del numero.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [DEFAULT](#DEFAULT) | Specifica che i numeri sono visualizzati nella forma predefinita del font\\u2019s. |
| [PROPORTIONAL](#PROPORTIONAL) | Specifica che le forme dei numeri progettate come spaziatura proporzionale sono visualizzate se supportate dal font. |
| [TABULAR](#TABULAR) | Specifica che le forme dei numeri progettate come tabulari sono visualizzate se supportate dal font. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String numSpacingName)](#fromName-java.lang.String) |  |
| [getName(int numSpacing)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int numSpacing)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Specifica che i numeri sono visualizzati nella forma predefinita del font\\u2019s.

### PROPORTIONAL {#PROPORTIONAL}
```
public static int PROPORTIONAL
```


Specifica che le forme dei numeri progettate come spaziatura proporzionale sono visualizzate se supportate dal font.

### TABULAR {#TABULAR}
```
public static int TABULAR
```


Specifica che le forme dei numeri progettate come tabulari sono visualizzate se supportate dal font.

### length {#length}
```
public static int length
```


### fromName(String numSpacingName) {#fromName-java.lang.String}
```
public static int fromName(String numSpacingName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| numSpacingName | java.lang.String |  |

**Returns:**
int
### getName(int numSpacing) {#getName-int}
```
public static String getName(int numSpacing)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| numSpacing | int |  |

**Returns:**
java.lang.String
