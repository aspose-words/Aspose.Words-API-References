---
title: ContinuousSectionRestart
second_title: Aspose.Words for Java API Reference
description: A utility class providing constants.
type: docs
weight: 93
url: /java/com.aspose.words/continuoussectionrestart/
---

**Inheritance:**
java.lang.Object
```
public class ContinuousSectionRestart
```

A utility class providing constants. Represents different behaviors when computing page numbers in a continuous section that restarts page numbering.
## Fields

| Field | Description |
| --- | --- |
| [ALWAYS](#ALWAYS) | Page numbering always restarts regardless of content flow. |
| [FROM_NEW_PAGE_ONLY](#FROM-NEW-PAGE-ONLY) | Page numbering restarts only if there is no other content before the section on the page where the section starts. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int continuousSectionRestart)](#getName-int-) |  |
| [toString(int continuousSectionRestart)](#toString-int-) |  |
| [fromName(String continuousSectionRestartName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### ALWAYS {#ALWAYS}
```
public static int ALWAYS
```


Page numbering always restarts regardless of content flow. This behavior is demonstrated by all MS Word versions, except Word 2016.

### FROM_NEW_PAGE_ONLY {#FROM-NEW-PAGE-ONLY}
```
public static int FROM_NEW_PAGE_ONLY
```


Page numbering restarts only if there is no other content before the section on the page where the section starts. The behavior is demonstrated by MS Word 2016.

### length {#length}
```
public static int length
```


### getName(int continuousSectionRestart) {#getName-int-}
```
public static String getName(int continuousSectionRestart)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| continuousSectionRestart | int |  |

**Returns:**
java.lang.String
### toString(int continuousSectionRestart) {#toString-int-}
```
public static String toString(int continuousSectionRestart)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| continuousSectionRestart | int |  |

**Returns:**
java.lang.String
### fromName(String continuousSectionRestartName) {#fromName-java.lang.String-}
```
public static int fromName(String continuousSectionRestartName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| continuousSectionRestartName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
