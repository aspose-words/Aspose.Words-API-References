---
title: "LineNumberRestartMode"
linktitle: "LineNumberRestartMode"
second_title: "Aspose.Words para Java"
description: "Determina cuándo se reinicia la numeración automática de líneas en Java."
type: docs
weight: 422
url: /es/java/com.aspose.words/linenumberrestartmode/
---

**Inheritance:**
java.lang.Object
```
public class LineNumberRestartMode
```

Determina cuándo se reinicia la numeración automática de líneas.

 **Examples:** 

Muestra cómo habilitar la numeración de líneas para una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [CONTINUOUS](#CONTINUOUS) | Numeración de líneas continua desde la sección anterior. |
| [RESTART_PAGE](#RESTART-PAGE) | La numeración de líneas se reinicia al comienzo de cada página. |
| [RESTART_SECTION](#RESTART-SECTION) | La numeración de líneas se reinicia al inicio de la sección. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String lineNumberRestartModeName)](#fromName-java.lang.String) |  |
| [getName(int lineNumberRestartMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int lineNumberRestartMode)](#toString-int) |  |
### CONTINUOUS {#CONTINUOUS}
```
public static int CONTINUOUS
```


Numeración de líneas continua desde la sección anterior.

### RESTART_PAGE {#RESTART-PAGE}
```
public static int RESTART_PAGE
```


La numeración de líneas se reinicia al comienzo de cada página.

### RESTART_SECTION {#RESTART-SECTION}
```
public static int RESTART_SECTION
```


La numeración de líneas se reinicia al inicio de la sección.

### length {#length}
```
public static int length
```


### fromName(String lineNumberRestartModeName) {#fromName-java.lang.String}
```
public static int fromName(String lineNumberRestartModeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| lineNumberRestartModeName | java.lang.String |  |

**Returns:**
int
### getName(int lineNumberRestartMode) {#getName-int}
```
public static String getName(int lineNumberRestartMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| lineNumberRestartMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int lineNumberRestartMode) {#toString-int}
```
public static String toString(int lineNumberRestartMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| lineNumberRestartMode | int |  |

**Returns:**
java.lang.String
