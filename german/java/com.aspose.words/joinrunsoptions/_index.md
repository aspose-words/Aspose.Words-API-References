---
title: "JoinRunsOptions"
linktitle: "JoinRunsOptions"
second_title: "Aspose.Words für Java"
description: "Stellt Konfigurationsflags für die Join‑Runs‑Operation in Java bereit."
type: docs
weight: 406
url: /de/java/com.aspose.words/joinrunsoptions/
---

**Inheritance:**
java.lang.Object
```
public class JoinRunsOptions
```

Stellt Konfigurationsflags für die Join‑Runs‑Operation bereit.

 **Examples:** 

Zeigt, wie man Runs mit derselben Formatierung zusammenführt, wobei redundante und unbedeutende Attribute ignoriert werden.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create runs with identical visible formatting but some internal differences.
 builder.getFont().setName("Arial");
 builder.getFont().setSize(12.0);
 builder.write("Hello ");
 builder.write("world");

 // Verify runs before join.
 Assert.assertEquals(2, doc.getFirstSection().getBody().getFirstParagraph().getRuns().getCount());
 Assert.assertEquals("Hello ", doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).getText());
 Assert.assertEquals("world", doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(1).getText());

 // Configure options to ignore redundant and insignificant attributes during join.
 JoinRunsOptions options = new JoinRunsOptions();
 options.setIgnoreRedundant(true); // Ignore redundant run properties that don't affect appearance.
 options.setIgnoreInsignificant(true); // Ignore insignificant differences like whitespace-only runs.

 // Join runs that have the same visible formatting using the extended options.
 doc.getFirstSection().getBody().getFirstParagraph().joinRunsWithSameFormatting(options);

 // Verify that runs were successfully joined.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getFirstParagraph().getRuns().getCount());
 Assert.assertEquals("Hello world", doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).getText());

 doc.save(getArtifactsDir() + "Paragraph.JoinRunsWithSameFormattingWithOptions.docx");
 
```
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getIgnoreInsignificant()](#getIgnoreInsignificant) | True gibt an, dass die unbedeutenden Attribute aller Runs beim Zusammenführen von Runs mit gleicher Formatierung ignoriert werden. |
| [getIgnoreRedundant()](#getIgnoreRedundant) | True gibt an, dass die redundanten Attribute aller Läufe ignoriert werden, wenn Läufe mit gleicher Formatierung zusammengeführt werden. |
| [getIgnoreSpacing()](#getIgnoreSpacing) | True gibt an, dass die Abstandsattribute aller Läufe ignoriert werden, wenn Läufe mit gleicher Formatierung zusammengeführt werden. |
| [setIgnoreInsignificant(boolean value)](#setIgnoreInsignificant-boolean) | True gibt an, dass die unbedeutenden Attribute aller Runs beim Zusammenführen von Runs mit gleicher Formatierung ignoriert werden. |
| [setIgnoreRedundant(boolean value)](#setIgnoreRedundant-boolean) | True gibt an, dass die redundanten Attribute aller Läufe ignoriert werden, wenn Läufe mit gleicher Formatierung zusammengeführt werden. |
| [setIgnoreSpacing(boolean value)](#setIgnoreSpacing-boolean) | True gibt an, dass die Abstandsattribute aller Läufe ignoriert werden, wenn Läufe mit gleicher Formatierung zusammengeführt werden. |
### getIgnoreInsignificant() {#getIgnoreInsignificant}
```
public boolean getIgnoreInsignificant()
```


True gibt an, dass die unbedeutenden Attribute aller Runs beim Zusammenführen von Runs mit gleicher Formatierung ignoriert werden.

 **Remarks:** 

Unbedeutende Attribute sind solche Attribute, die keinen spürbaren Einfluss auf die Formatierung eines Laufs mit dem angegebenen Textinhalt haben. Der Standardwert ist False.

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getIgnoreRedundant() {#getIgnoreRedundant}
```
public boolean getIgnoreRedundant()
```


True gibt an, dass die redundanten Attribute aller Läufe ignoriert werden, wenn Läufe mit gleicher Formatierung zusammengeführt werden.

 **Remarks:** 

Redundante Attribute sind solche Attribute, die den Lauf mit dem angegebenen Textinhalt nicht beeinflussen. Der Standardwert ist False.

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getIgnoreSpacing() {#getIgnoreSpacing}
```
public boolean getIgnoreSpacing()
```


True gibt an, dass die Abstandsattribute aller Läufe ignoriert werden, wenn Läufe mit gleicher Formatierung zusammengeführt werden.

 **Remarks:** 

Der Standardwert ist False.

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### setIgnoreInsignificant(boolean value) {#setIgnoreInsignificant-boolean}
```
public void setIgnoreInsignificant(boolean value)
```


True gibt an, dass die unbedeutenden Attribute aller Runs beim Zusammenführen von Runs mit gleicher Formatierung ignoriert werden.

 **Remarks:** 

Unbedeutende Attribute sind solche Attribute, die keinen spürbaren Einfluss auf die Formatierung eines Laufs mit dem angegebenen Textinhalt haben. Der Standardwert ist False.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setIgnoreRedundant(boolean value) {#setIgnoreRedundant-boolean}
```
public void setIgnoreRedundant(boolean value)
```


True gibt an, dass die redundanten Attribute aller Läufe ignoriert werden, wenn Läufe mit gleicher Formatierung zusammengeführt werden.

 **Remarks:** 

Redundante Attribute sind solche Attribute, die den Lauf mit dem angegebenen Textinhalt nicht beeinflussen. Der Standardwert ist False.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setIgnoreSpacing(boolean value) {#setIgnoreSpacing-boolean}
```
public void setIgnoreSpacing(boolean value)
```


True gibt an, dass die Abstandsattribute aller Läufe ignoriert werden, wenn Läufe mit gleicher Formatierung zusammengeführt werden.

 **Remarks:** 

Der Standardwert ist False.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

