---
title: HeightRule
second_title: Aspose.Words for Java API Reference
description: A utility class providing constants.
type: docs
weight: 319
url: /java/com.aspose.words/heightrule/
---

**Inheritance:**
java.lang.Object
```
public class HeightRule
```

A utility class providing constants. Specifies the rule for determining the height of an object.
## Fields

| Field | Description |
| --- | --- |
| [AT_LEAST](#AT-LEAST) | The height will be at least the specified height in points. |
| [EXACTLY](#EXACTLY) | The height is specified exactly in points. |
| [AUTO](#AUTO) | The height will grow automatically to accommodate all text inside an object. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int heightRule)](#getName-int-) |  |
| [toString(int heightRule)](#toString-int-) |  |
| [fromName(String heightRuleName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### AT_LEAST {#AT-LEAST}
```
public static int AT_LEAST
```


The height will be at least the specified height in points. It will grow, if needed, to accommodate all text inside an object.

### EXACTLY {#EXACTLY}
```
public static int EXACTLY
```


The height is specified exactly in points. Please note that if the text cannot fit inside the object of this height, it will appear truncated.

### AUTO {#AUTO}
```
public static int AUTO
```


The height will grow automatically to accommodate all text inside an object.

### length {#length}
```
public static int length
```


### getName(int heightRule) {#getName-int-}
```
public static String getName(int heightRule)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| heightRule | int |  |

**Returns:**
java.lang.String
### toString(int heightRule) {#toString-int-}
```
public static String toString(int heightRule)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| heightRule | int |  |

**Returns:**
java.lang.String
### fromName(String heightRuleName) {#fromName-java.lang.String-}
```
public static int fromName(String heightRuleName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| heightRuleName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
