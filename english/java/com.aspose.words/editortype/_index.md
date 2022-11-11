---
title: EditorType
second_title: Aspose.Words for Java API Reference
description: Specifies the set of possible aliases or editing groups which can be used as aliases to determine if the current user shall be allowed to edit a single range defined by an editable range within a document.
type: docs
weight: 140
url: /java/com.aspose.words/editortype/
---

**Inheritance:**
java.lang.Object
```
public class EditorType
```

Specifies the set of possible aliases (or editing groups) which can be used as aliases to determine if the current user shall be allowed to edit a single range defined by an editable range within a document.
## Fields

| Field | Description |
| --- | --- |
| [ADMINISTRATORS](#ADMINISTRATORS) | Specifies that users associated with the Administrators group shall be allowed to edit editable ranges using this editing type when document protection is enabled. |
| [CONTRIBUTORS](#CONTRIBUTORS) | Specifies that users associated with the Contributors group shall be allowed to edit editable ranges using this editing type when document protection is enabled. |
| [CURRENT](#CURRENT) | Specifies that users associated with the Current group shall be allowed to edit editable ranges using this editing type when document protection is enabled. |
| [DEFAULT](#DEFAULT) | Same as [UNSPECIFIED](../../com.aspose.words/editortype\#UNSPECIFIED). |
| [EDITORS](#EDITORS) | Specifies that users associated with the Editors group shall be allowed to edit editable ranges using this editing type when document protection is enabled. |
| [EVERYONE](#EVERYONE) | Specifies that all users that open the document shall be allowed to edit editable ranges using this editing type when document protection is enabled. |
| [NONE](#NONE) | Specifies that none of the users that open the document shall be allowed to edit editable ranges using this editing type when document protection is enabled. |
| [OWNERS](#OWNERS) | Specifies that users associated with the Owners group shall be allowed to edit editable ranges using this editing type when document protection is enabled. |
| [UNSPECIFIED](#UNSPECIFIED) | Means that editor type is not specified. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String editorTypeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int editorType)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int editorType)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### ADMINISTRATORS {#ADMINISTRATORS}
```
public static int ADMINISTRATORS
```


Specifies that users associated with the Administrators group shall be allowed to edit editable ranges using this editing type when document protection is enabled.

### CONTRIBUTORS {#CONTRIBUTORS}
```
public static int CONTRIBUTORS
```


Specifies that users associated with the Contributors group shall be allowed to edit editable ranges using this editing type when document protection is enabled.

### CURRENT {#CURRENT}
```
public static int CURRENT
```


Specifies that users associated with the Current group shall be allowed to edit editable ranges using this editing type when document protection is enabled.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Same as [UNSPECIFIED](../../com.aspose.words/editortype\#UNSPECIFIED).

### EDITORS {#EDITORS}
```
public static int EDITORS
```


Specifies that users associated with the Editors group shall be allowed to edit editable ranges using this editing type when document protection is enabled.

### EVERYONE {#EVERYONE}
```
public static int EVERYONE
```


Specifies that all users that open the document shall be allowed to edit editable ranges using this editing type when document protection is enabled.

### NONE {#NONE}
```
public static int NONE
```


Specifies that none of the users that open the document shall be allowed to edit editable ranges using this editing type when document protection is enabled.

### OWNERS {#OWNERS}
```
public static int OWNERS
```


Specifies that users associated with the Owners group shall be allowed to edit editable ranges using this editing type when document protection is enabled.

### UNSPECIFIED {#UNSPECIFIED}
```
public static int UNSPECIFIED
```


Means that editor type is not specified.

### length {#length}
```
public static int length
```


### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### fromName(String editorTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String editorTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| editorTypeName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int editorType) {#getName-int-}
```
public static String getName(int editorType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| editorType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### toString() {#toString--}
```
public String toString()
```




**Returns:**
java.lang.String
### toString(int editorType) {#toString-int-}
```
public static String toString(int editorType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| editorType | int |  |

**Returns:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

