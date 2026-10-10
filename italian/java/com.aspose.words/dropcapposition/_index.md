---
title: "DropCapPosition"
linktitle: "DropCapPosition"
second_title: "Aspose.Words per Java"
description: "Specifica la posizione del testo a capostipite in Java."
type: docs
weight: 177
url: /it/java/com.aspose.words/dropcapposition/
---

**Inheritance:**
java.lang.Object
```
public class DropCapPosition
```

Specifica la posizione per un testo con capoverso iniziale.

 **Examples:** 

Mostra come creare un capostipite.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert one paragraph with a large letter that the text in the second and third paragraphs begins with.
 builder.getFont().setSize(54.0);
 builder.writeln("L");

 builder.getFont().setSize(18.0);
 builder.writeln("orem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
 builder.writeln("Ut enim ad minim veniam, quis nostrud exercitation " +
         "ullamco laboris nisi ut aliquip ex ea commodo consequat.");

 // Currently, the second and third paragraphs will appear underneath the first.
 // We can convert the first paragraph as a drop cap for the other paragraphs via its "ParagraphFormat" object.
 // Set the "DropCapPosition" property to "DropCapPosition.Margin" to place the drop cap
 // outside the left-hand side page margin if our text is left-to-right.
 // Set the "DropCapPosition" property to "DropCapPosition.Normal" to place the drop cap within the page margins
 // and to wrap the rest of the text around it.
 // "DropCapPosition.None" is the default state for all paragraphs.
 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();
 format.setDropCapPosition(dropCapPosition);

 doc.save(getArtifactsDir() + "ParagraphFormat.DropCap.docx");
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [MARGIN](#MARGIN) | Il capostipite è posizionato al di fuori del margine del testo nel paragrafo di ancoraggio. |
| [NONE](#NONE) | Il paragrafo non ha un capostipite. |
| [NORMAL](#NORMAL) | Il capostipite è posizionato all'interno del margine del testo nel paragrafo di ancoraggio. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String dropCapPositionName)](#fromName-java.lang.String) |  |
| [getName(int dropCapPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int dropCapPosition)](#toString-int) |  |
### MARGIN {#MARGIN}
```
public static int MARGIN
```


Il capostipite è posizionato al di fuori del margine del testo nel paragrafo di ancoraggio.

### NONE {#NONE}
```
public static int NONE
```


Il paragrafo non ha un capostipite.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Il capostipite è posizionato all'interno del margine del testo nel paragrafo di ancoraggio.

### length {#length}
```
public static int length
```


### fromName(String dropCapPositionName) {#fromName-java.lang.String}
```
public static int fromName(String dropCapPositionName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| dropCapPositionName | java.lang.String |  |

**Returns:**
int
### getName(int dropCapPosition) {#getName-int}
```
public static String getName(int dropCapPosition)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| dropCapPosition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int dropCapPosition) {#toString-int}
```
public static String toString(int dropCapPosition)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| dropCapPosition | int |  |

**Returns:**
java.lang.String
