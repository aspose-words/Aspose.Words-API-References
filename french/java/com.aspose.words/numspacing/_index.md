---
title: "NumSpacing"
linktitle: "NumSpacing"
second_title: "Aspose.Words pour Java"
description: "Spécifie les valeurs possibles dans lesquelles l’espacement des chiffres peut être affiché en Java."
type: docs
weight: 484
url: /fr/java/com.aspose.words/numspacing/
---

**Inheritance:**
java.lang.Object
```
public class NumSpacing
```

Spécifie les valeurs possibles dans lesquelles l'espacement des chiffres peut être affiché.

 **Examples:** 

Montre comment définir le type d’espacement du chiffre.

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
## Champs

| Champ | Description |
| --- | --- |
| [DEFAULT](#DEFAULT) | Spécifie que les chiffres sont affichés sous la forme par défaut de la police\\u2019s. |
| [PROPORTIONAL](#PROPORTIONAL) | Spécifie que les formes des chiffres conçues comme proportionnellement espacées sont affichées si la police le prend en charge. |
| [TABULAR](#TABULAR) | Spécifie que les formes des chiffres conçues comme tabulaires sont affichées si la police le prend en charge. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String numSpacingName)](#fromName-java.lang.String) |  |
| [getName(int numSpacing)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int numSpacing)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Spécifie que les chiffres sont affichés sous la forme par défaut de la police\\u2019s.

### PROPORTIONAL {#PROPORTIONAL}
```
public static int PROPORTIONAL
```


Spécifie que les formes des chiffres conçues comme proportionnellement espacées sont affichées si la police le prend en charge.

### TABULAR {#TABULAR}
```
public static int TABULAR
```


Spécifie que les formes des chiffres conçues comme tabulaires sont affichées si la police le prend en charge.

### length {#length}
```
public static int length
```


### fromName(String numSpacingName) {#fromName-java.lang.String}
```
public static int fromName(String numSpacingName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| numSpacingName | java.lang.String |  |

**Returns:**
int
### getName(int numSpacing) {#getName-int}
```
public static String getName(int numSpacing)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| numSpacing | int |  |

**Returns:**
java.lang.String
