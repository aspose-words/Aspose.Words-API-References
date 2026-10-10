---
title: "ShowInBalloons"
linktitle: "ShowInBalloons"
second_title: "Aspose.Words Java için"
description: "Java'da balonlarda hangi revizyonların gösterileceğini belirtir."
type: docs
weight: 619
url: /tr/java/com.aspose.words/showinballoons/
---

**Inheritance:**
java.lang.Object
```
public class ShowInBalloons
```

Balonlarda hangi revizyonların gösterileceğini belirtir.

 **Remarks:** 

Revizyonların [CommentDisplayMode.SHOW_IN_ANNOTATIONS](../../com.aspose.words/commentdisplaymode/\\#SHOW-IN-ANNOTATIONS) için balonlarda renderlenmediğini unutmayın.

 **Examples:** 

Revizyonların görünümünü nasıl değiştireceğinizi gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [FORMAT](#FORMAT) | Ekleme ve silme revizyonlarını satır içinde, format revizyonlarını balonlarda gösterir. |
| [FORMAT_AND_DELETE](#FORMAT-AND-DELETE) | Ekleme revizyonlarını satır içinde, silme ve format revizyonlarını balonlarda gösterir. |
| [NONE](#NONE) | Ekleme, silme ve format revizyonlarını satır içinde gösterir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String showInBalloonsName)](#fromName-java.lang.String) |  |
| [getName(int showInBalloons)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int showInBalloons)](#toString-int) |  |
### FORMAT {#FORMAT}
```
public static int FORMAT
```


Ekleme ve silme revizyonlarını satır içinde, format revizyonlarını balonlarda gösterir.

### FORMAT_AND_DELETE {#FORMAT-AND-DELETE}
```
public static int FORMAT_AND_DELETE
```


Ekleme revizyonlarını satır içinde, silme ve format revizyonlarını balonlarda gösterir.

### NONE {#NONE}
```
public static int NONE
```


Ekleme, silme ve format revizyonlarını satır içinde gösterir.

### length {#length}
```
public static int length
```


### fromName(String showInBalloonsName) {#fromName-java.lang.String}
```
public static int fromName(String showInBalloonsName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| showInBalloonsName | java.lang.String |  |

**Returns:**
int
### getName(int showInBalloons) {#getName-int}
```
public static String getName(int showInBalloons)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| showInBalloons | int |  |

**Returns:**
java.lang.String
