---
title: ShowInBalloons
linktitle: ShowInBalloons
second_title: Aspose.Words for Java
description: Specifies which revisions are rendered in balloons in Java.
type: docs
weight: 599
url: /java/com.aspose.words/showinballoons/
---

**Inheritance:**
java.lang.Object
```
public class ShowInBalloons
```

Specifies which revisions are rendered in balloons.

 **Remarks:** 

Note that revisions are not rendered in balloons for [CommentDisplayMode.SHOW\_IN\_ANNOTATIONS](../../com.aspose.words/commentdisplaymode/\#SHOW-IN-ANNOTATIONS).

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
| [FORMAT](#FORMAT) | Renders insert and delete revisions inline, format revisions in balloons. |
| [FORMAT_AND_DELETE](#FORMAT-AND-DELETE) | Renders insert revisions inline, delete and format revisions in balloons. |
| [NONE](#NONE) | Renders insert, delete and format revisions inline. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String showInBalloonsName)](#fromName-java.lang.String) |  |
| [getName(int showInBalloons)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int showInBalloons)](#toString-int) |  |
### FORMAT {#FORMAT}
```
public static int FORMAT
```


Renders insert and delete revisions inline, format revisions in balloons.

### FORMAT_AND_DELETE {#FORMAT-AND-DELETE}
```
public static int FORMAT_AND_DELETE
```


Renders insert revisions inline, delete and format revisions in balloons.

### NONE {#NONE}
```
public static int NONE
```


Renders insert, delete and format revisions inline.

### length {#length}
```
public static int length
```


### fromName(String showInBalloonsName) {#fromName-java.lang.String}
```
public static int fromName(String showInBalloonsName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| showInBalloonsName | java.lang.String |  |

**Returns:**
int
### getName(int showInBalloons) {#getName-int}
```
public static String getName(int showInBalloons)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| showInBalloons | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int showInBalloons) {#toString-int}
```
public static String toString(int showInBalloons)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| showInBalloons | int |  |

**Returns:**
java.lang.String
