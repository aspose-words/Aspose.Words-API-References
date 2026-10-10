---
title: "NumSpacing"
linktitle: "NumSpacing"
second_title: "Aspose.Words für Java"
description: "Gibt mögliche Werte an, in denen die Ziffernabstände in Java angezeigt werden können."
type: docs
weight: 484
url: /de/java/com.aspose.words/numspacing/
---

**Inheritance:**
java.lang.Object
```
public class NumSpacing
```

Gibt mögliche Werte an, in denen die Ziffernabstände angezeigt werden können.

 **Examples:** 

Zeigt, wie der Abstandstyp der Ziffer festgelegt wird.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [DEFAULT](#DEFAULT) | Gibt an, dass Ziffern in der Standardschriftform der Schriftart angezeigt werden. |
| [PROPORTIONAL](#PROPORTIONAL) | Gibt an, dass die Formen der Ziffern, die proportional angeordnet sind, angezeigt werden, wenn die Schriftart dies unterstützt. |
| [TABULAR](#TABULAR) | Gibt an, dass die Formen der Ziffern, die tabellarisch angeordnet sind, angezeigt werden, wenn die Schriftart dies unterstützt. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String numSpacingName)](#fromName-java.lang.String) |  |
| [getName(int numSpacing)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int numSpacing)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Gibt an, dass Ziffern in der Standardschriftform der Schriftart angezeigt werden.

### PROPORTIONAL {#PROPORTIONAL}
```
public static int PROPORTIONAL
```


Gibt an, dass die Formen der Ziffern, die proportional angeordnet sind, angezeigt werden, wenn die Schriftart dies unterstützt.

### TABULAR {#TABULAR}
```
public static int TABULAR
```


Gibt an, dass die Formen der Ziffern, die tabellarisch angeordnet sind, angezeigt werden, wenn die Schriftart dies unterstützt.

### length {#length}
```
public static int length
```


### fromName(String numSpacingName) {#fromName-java.lang.String}
```
public static int fromName(String numSpacingName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| numSpacingName | java.lang.String |  |

**Returns:**
int
### getName(int numSpacing) {#getName-int}
```
public static String getName(int numSpacing)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| numSpacing | int |  |

**Returns:**
java.lang.String
