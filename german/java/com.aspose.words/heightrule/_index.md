---
title: "HeightRule"
linktitle: "HeightRule"
second_title: "Aspose.Words für Java"
description: "Gibt die Regel zur Bestimmung der Höhe eines Objekts in Java an."
type: docs
weight: 373
url: /de/java/com.aspose.words/heightrule/
---

**Inheritance:**
java.lang.Object
```
public class HeightRule
```

Legt die Regel zur Bestimmung der Höhe eines Objekts fest.

 **Examples:** 

Zeigt, wie man Zeilen mit einem DocumentBuilder formatiert.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Start a second row, and then configure its height. The builder will apply these settings to
 // its current row, as well as any new rows it creates afterwards.
 builder.endRow();

 RowFormat rowFormat = builder.getRowFormat();
 rowFormat.setHeight(100.0);
 rowFormat.setHeightRule(HeightRule.EXACTLY);

 builder.insertCell();
 builder.write("Row 2, cell 1.");
 builder.endTable();

 // The first row was unaffected by the padding reconfiguration and still holds the default values.
 Assert.assertEquals(0.0d, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());

 Assert.assertEquals(100.0d, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());

 doc.save(getArtifactsDir() + "DocumentBuilder.SetRowFormatting.docx");
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [AT_LEAST](#AT-LEAST) | Die Höhe wird mindestens die angegebene Höhe in Punkten betragen. |
| [AUTO](#AUTO) | Die Höhe wird automatisch wachsen, um den gesamten Text im Inneren eines Objekts aufzunehmen. |
| [EXACTLY](#EXACTLY) | Die Höhe wird exakt in Punkten angegeben. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String heightRuleName)](#fromName-java.lang.String) |  |
| [getName(int heightRule)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int heightRule)](#toString-int) |  |
### AT_LEAST {#AT-LEAST}
```
public static int AT_LEAST
```


Die Höhe wird mindestens die angegebene Höhe in Punkten betragen. Sie wird bei Bedarf wachsen, um den gesamten Text im Inneren eines Objekts aufzunehmen.

### AUTO {#AUTO}
```
public static int AUTO
```


Die Höhe wird automatisch wachsen, um den gesamten Text im Inneren eines Objekts aufzunehmen.

### EXACTLY {#EXACTLY}
```
public static int EXACTLY
```


Die Höhe wird exakt in Punkten angegeben. Bitte beachten Sie, dass der Text, wenn er nicht in das Objekt dieser Höhe passt, abgeschnitten wird.

### length {#length}
```
public static int length
```


### fromName(String heightRuleName) {#fromName-java.lang.String}
```
public static int fromName(String heightRuleName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| heightRuleName | java.lang.String |  |

**Returns:**
int
### getName(int heightRule) {#getName-int}
```
public static String getName(int heightRule)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| heightRule | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int heightRule) {#toString-int}
```
public static String toString(int heightRule)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| heightRule | int |  |

**Returns:**
java.lang.String
