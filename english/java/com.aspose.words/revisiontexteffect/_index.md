---
title: RevisionTextEffect
linktitle: RevisionTextEffect
second_title: Aspose.Words for Java
description: Allows to specify decoration effect for revisions of document text in Java.
type: docs
weight: 509
url: /java/com.aspose.words/revisiontexteffect/
---

**Inheritance:**
java.lang.Object
```
public class RevisionTextEffect
```

Allows to specify decoration effect for revisions of document text.

 **Examples:** 

Shows how to modify the appearance of revisions.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```
## Fields

| Field | Description |
| --- | --- |
| [BOLD](#BOLD) | Revised content is made bold and colored. |
| [COLOR](#COLOR) | Revised content is highlighted with color only. |
| [DOUBLE_STRIKE_THROUGH](#DOUBLE-STRIKE-THROUGH) | Revised content is double stroked through and colored. |
| [DOUBLE_UNDERLINE](#DOUBLE-UNDERLINE) | Revised content is double underlined and colored. |
| [HIDDEN](#HIDDEN) | Revised content is hidden. |
| [ITALIC](#ITALIC) | Revised content is made italic and colored. |
| [NONE](#NONE) | Revised content has no special effects applied. |
| [STRIKE_THROUGH](#STRIKE-THROUGH) | Revised content is stroked through and colored. |
| [UNDERLINE](#UNDERLINE) | Revised content is underlined and colored. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String revisionTextEffectName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int revisionTextEffect)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int revisionTextEffect)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### BOLD {#BOLD}
```
public static int BOLD
```


Revised content is made bold and colored.

### COLOR {#COLOR}
```
public static int COLOR
```


Revised content is highlighted with color only.

### DOUBLE_STRIKE_THROUGH {#DOUBLE-STRIKE-THROUGH}
```
public static int DOUBLE_STRIKE_THROUGH
```


Revised content is double stroked through and colored.

 **Remarks:** 

Only works for [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION), [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE) and [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING) ('move from' type).

### DOUBLE_UNDERLINE {#DOUBLE-UNDERLINE}
```
public static int DOUBLE_UNDERLINE
```


Revised content is double underlined and colored.

### HIDDEN {#HIDDEN}
```
public static int HIDDEN
```


Revised content is hidden.

 **Remarks:** 

Only works for [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION) and [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING) ('move from' type).

### ITALIC {#ITALIC}
```
public static int ITALIC
```


Revised content is made italic and colored.

### NONE {#NONE}
```
public static int NONE
```


Revised content has no special effects applied. This corresponds to [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT).

### STRIKE_THROUGH {#STRIKE-THROUGH}
```
public static int STRIKE_THROUGH
```


Revised content is stroked through and colored.

### UNDERLINE {#UNDERLINE}
```
public static int UNDERLINE
```


Revised content is underlined and colored.

### length {#length}
```
public static int length
```


### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### fromName(String revisionTextEffectName) {#fromName-java.lang.String}
```
public static int fromName(String revisionTextEffectName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| revisionTextEffectName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int revisionTextEffect) {#getName-int}
```
public static String getName(int revisionTextEffect)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| revisionTextEffect | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### toString(int revisionTextEffect) {#toString-int}
```
public static String toString(int revisionTextEffect)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| revisionTextEffect | int |  |

**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

