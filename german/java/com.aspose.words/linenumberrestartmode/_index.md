---
title: "LineNumberRestartMode"
linktitle: "LineNumberRestartMode"
second_title: "Aspose.Words für Java"
description: "Bestimmt, wann die automatische Zeilennummerierung in Java neu startet."
type: docs
weight: 422
url: /de/java/com.aspose.words/linenumberrestartmode/
---

**Inheritance:**
java.lang.Object
```
public class LineNumberRestartMode
```

Bestimmt, wann die automatische Zeilennummerierung neu startet.

 **Examples:** 

Zeigt, wie man die Zeilennummerierung für einen Abschnitt aktiviert.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [CONTINUOUS](#CONTINUOUS) | Die Zeilennummerierung ist fortlaufend aus dem vorherigen Abschnitt. |
| [RESTART_PAGE](#RESTART-PAGE) | Die Zeilennummerierung startet zu Beginn jeder Seite neu. |
| [RESTART_SECTION](#RESTART-SECTION) | Die Zeilennummerierung startet zu Beginn des Abschnitts neu. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String lineNumberRestartModeName)](#fromName-java.lang.String) |  |
| [getName(int lineNumberRestartMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int lineNumberRestartMode)](#toString-int) |  |
### CONTINUOUS {#CONTINUOUS}
```
public static int CONTINUOUS
```


Die Zeilennummerierung ist fortlaufend aus dem vorherigen Abschnitt.

### RESTART_PAGE {#RESTART-PAGE}
```
public static int RESTART_PAGE
```


Die Zeilennummerierung startet zu Beginn jeder Seite neu.

### RESTART_SECTION {#RESTART-SECTION}
```
public static int RESTART_SECTION
```


Die Zeilennummerierung startet zu Beginn des Abschnitts neu.

### length {#length}
```
public static int length
```


### fromName(String lineNumberRestartModeName) {#fromName-java.lang.String}
```
public static int fromName(String lineNumberRestartModeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| lineNumberRestartModeName | java.lang.String |  |

**Returns:**
int
### getName(int lineNumberRestartMode) {#getName-int}
```
public static String getName(int lineNumberRestartMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| lineNumberRestartMode | int |  |

**Returns:**
java.lang.String
