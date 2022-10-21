---
title: ResourceLoadingAction
second_title: Aspose.Words for Java API Reference
description: A utility class providing constants.
type: docs
weight: 479
url: /java/com.aspose.words/resourceloadingaction/
---

**Inheritance:**
java.lang.Object
```
public class ResourceLoadingAction
```

A utility class providing constants. Specifies the mode of resource loading.

To learn more, visit the **Specify Load Options** documentation article.
## Fields

| Field | Description |
| --- | --- |
| [DEFAULT](#DEFAULT) | Aspose.Words will load this resource as usual. |
| [SKIP](#SKIP) | Aspose.Words will skip loading of this resource. |
| [USER_PROVIDED](#USER-PROVIDED) | Aspose.Words will use byte array provided by user in [ResourceLoadingArgs.setData(byte[])](../../com.aspose.words/resourceloadingargs\#setData-byte---) as resource data. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int resourceLoadingAction)](#getName-int-) |  |
| [toString(int resourceLoadingAction)](#toString-int-) |  |
| [fromName(String resourceLoadingActionName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Aspose.Words will load this resource as usual.

### SKIP {#SKIP}
```
public static int SKIP
```


Aspose.Words will skip loading of this resource. Only link without data will be stored for an image, CSS style sheet will be ignored for HTML format.

### USER_PROVIDED {#USER-PROVIDED}
```
public static int USER_PROVIDED
```


Aspose.Words will use byte array provided by user in [ResourceLoadingArgs.setData(byte[])](../../com.aspose.words/resourceloadingargs\#setData-byte---) as resource data.

### length {#length}
```
public static int length
```


### getName(int resourceLoadingAction) {#getName-int-}
```
public static String getName(int resourceLoadingAction)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| resourceLoadingAction | int |  |

**Returns:**
java.lang.String
### toString(int resourceLoadingAction) {#toString-int-}
```
public static String toString(int resourceLoadingAction)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| resourceLoadingAction | int |  |

**Returns:**
java.lang.String
### fromName(String resourceLoadingActionName) {#fromName-java.lang.String-}
```
public static int fromName(String resourceLoadingActionName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| resourceLoadingActionName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
