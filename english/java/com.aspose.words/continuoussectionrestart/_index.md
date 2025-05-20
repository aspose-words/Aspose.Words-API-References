---
title: ContinuousSectionRestart
linktitle: ContinuousSectionRestart
second_title: Aspose.Words for Java
description: Represents different behaviors when computing page numbers in a continuous section that restarts page numbering in Java.
type: docs
weight: 127
url: /java/com.aspose.words/continuoussectionrestart/
---

**Inheritance:**
java.lang.Object
```
public class ContinuousSectionRestart
```

Represents different behaviors when computing page numbers in a continuous section that restarts page numbering.

 **Examples:** 

Shows how to control page numbering in a continuous section.

```

 Document doc = new Document(getMyDir() + "Continuous section page numbering.docx");

 // By default Aspose.Words behavior matches the Microsoft Word 2019.
 // If you need old Aspose.Words behavior, repetitive Microsoft Word 2016, use 'ContinuousSectionRestart.FromNewPageOnly'.
 // Page numbering restarts only if there is no other content before the section on the page where the section starts,
 // because of that the numbering will reset to 2 from the second page.
 doc.getLayoutOptions().setContinuousSectionPageNumberingRestart(ContinuousSectionRestart.FROM_NEW_PAGE_ONLY);
 doc.updatePageLayout();

 doc.save(getArtifactsDir() + "Layout.RestartPageNumberingInContinuousSection.pdf");
 
```
## Fields

| Field | Description |
| --- | --- |
| [ALWAYS](#ALWAYS) | Page numbering always restarts regardless of content flow. |
| [FROM_NEW_PAGE_ONLY](#FROM-NEW-PAGE-ONLY) | Page numbering restarts only if there is no other content before the section on the page where the section starts. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String continuousSectionRestartName)](#fromName-java.lang.String) |  |
| [getName(int continuousSectionRestart)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int continuousSectionRestart)](#toString-int) |  |
### ALWAYS {#ALWAYS}
```
public static int ALWAYS
```


Page numbering always restarts regardless of content flow.

 **Remarks:** 

This behavior is demonstrated by all MS Word versions, except Word 2016.

### FROM_NEW_PAGE_ONLY {#FROM-NEW-PAGE-ONLY}
```
public static int FROM_NEW_PAGE_ONLY
```


Page numbering restarts only if there is no other content before the section on the page where the section starts.

 **Remarks:** 

The behavior is demonstrated by MS Word 2016.

### length {#length}
```
public static int length
```


### fromName(String continuousSectionRestartName) {#fromName-java.lang.String}
```
public static int fromName(String continuousSectionRestartName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| continuousSectionRestartName | java.lang.String |  |

**Returns:**
int
### getName(int continuousSectionRestart) {#getName-int}
```
public static String getName(int continuousSectionRestart)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| continuousSectionRestart | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int continuousSectionRestart) {#toString-int}
```
public static String toString(int continuousSectionRestart)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| continuousSectionRestart | int |  |

**Returns:**
java.lang.String
