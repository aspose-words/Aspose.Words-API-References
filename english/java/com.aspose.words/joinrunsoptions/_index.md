---
title: JoinRunsOptions
linktitle: JoinRunsOptions
second_title: Aspose.Words for Java
description: Provides configuration flags for the join runs operation in Java.
type: docs
weight: 406
url: /java/com.aspose.words/joinrunsoptions/
---

**Inheritance:**
java.lang.Object
```
public class JoinRunsOptions
```

Provides configuration flags for the join runs operation.

 **Examples:** 

Shows how to join runs with the same formatting while ignoring redundant and insignificant attributes.

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
## Methods

| Method | Description |
| --- | --- |
| [getIgnoreInsignificant()](#getIgnoreInsignificant) | True indicates that the insignificant attributes of all runs will be ignored when joining runs with same formatting. |
| [getIgnoreRedundant()](#getIgnoreRedundant) | True indicates that the redundant attributes of all runs will be ignored when joining runs with same formatting. |
| [getIgnoreSpacing()](#getIgnoreSpacing) | True indicates that the spacing attributes of all runs will be ignored when joining runs with same formatting. |
| [setIgnoreInsignificant(boolean value)](#setIgnoreInsignificant-boolean) | True indicates that the insignificant attributes of all runs will be ignored when joining runs with same formatting. |
| [setIgnoreRedundant(boolean value)](#setIgnoreRedundant-boolean) | True indicates that the redundant attributes of all runs will be ignored when joining runs with same formatting. |
| [setIgnoreSpacing(boolean value)](#setIgnoreSpacing-boolean) | True indicates that the spacing attributes of all runs will be ignored when joining runs with same formatting. |
### getIgnoreInsignificant() {#getIgnoreInsignificant}
```
public boolean getIgnoreInsignificant()
```


True indicates that the insignificant attributes of all runs will be ignored when joining runs with same formatting.

 **Remarks:** 

Insignificant attributes are those attributes that do not have a noticeable effect on the formatting of a run with the given text content. The default value is False.

**Returns:**
boolean - The corresponding  boolean  value.
### getIgnoreRedundant() {#getIgnoreRedundant}
```
public boolean getIgnoreRedundant()
```


True indicates that the redundant attributes of all runs will be ignored when joining runs with same formatting.

 **Remarks:** 

Redundant attributes are those attributes that do not affect the run with the given text content. The default value is False.

**Returns:**
boolean - The corresponding  boolean  value.
### getIgnoreSpacing() {#getIgnoreSpacing}
```
public boolean getIgnoreSpacing()
```


True indicates that the spacing attributes of all runs will be ignored when joining runs with same formatting.

 **Remarks:** 

The default value is False.

**Returns:**
boolean - The corresponding  boolean  value.
### setIgnoreInsignificant(boolean value) {#setIgnoreInsignificant-boolean}
```
public void setIgnoreInsignificant(boolean value)
```


True indicates that the insignificant attributes of all runs will be ignored when joining runs with same formatting.

 **Remarks:** 

Insignificant attributes are those attributes that do not have a noticeable effect on the formatting of a run with the given text content. The default value is False.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setIgnoreRedundant(boolean value) {#setIgnoreRedundant-boolean}
```
public void setIgnoreRedundant(boolean value)
```


True indicates that the redundant attributes of all runs will be ignored when joining runs with same formatting.

 **Remarks:** 

Redundant attributes are those attributes that do not affect the run with the given text content. The default value is False.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setIgnoreSpacing(boolean value) {#setIgnoreSpacing-boolean}
```
public void setIgnoreSpacing(boolean value)
```


True indicates that the spacing attributes of all runs will be ignored when joining runs with same formatting.

 **Remarks:** 

The default value is False.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

