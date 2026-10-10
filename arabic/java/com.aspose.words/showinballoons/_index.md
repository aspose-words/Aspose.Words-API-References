---
title: "ShowInBalloons"
linktitle: "ShowInBalloons"
second_title: "Aspose.Words لـ Java"
description: "يحدد أي المراجعات تُعرض في الفقاعات في Java."
type: docs
weight: 619
url: /ar/java/com.aspose.words/showinballoons/
---

**Inheritance:**
java.lang.Object
```
public class ShowInBalloons
```

يحدد أي المراجعات يتم عرضها في الفقاعات.

 **Remarks:** 

لاحظ أن المراجعات لا تُعرض في الفقاعات لـ [CommentDisplayMode.SHOW\_IN\_ANNOTATIONS](../../com.aspose.words/commentdisplaymode/\#SHOW-IN-ANNOTATIONS).

 **Examples:** 

يظهر كيفية تعديل مظهر التعديلات.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [FORMAT](#FORMAT) | يعرض مراجعات الإدراج والحذف داخل السطر، ومراجعات التنسيق في الفقاعات. |
| [FORMAT_AND_DELETE](#FORMAT-AND-DELETE) | يعرض مراجعات الإدراج داخل السطر، ومراجعات الحذف والتنسيق في الفقاعات. |
| [NONE](#NONE) | يعرض مراجعات الإدراج والحذف والتنسيق داخل السطر. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String showInBalloonsName)](#fromName-java.lang.String) |  |
| [getName(int showInBalloons)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int showInBalloons)](#toString-int) |  |
### FORMAT {#FORMAT}
```
public static int FORMAT
```


يعرض مراجعات الإدراج والحذف داخل السطر، ومراجعات التنسيق في الفقاعات.

### FORMAT_AND_DELETE {#FORMAT-AND-DELETE}
```
public static int FORMAT_AND_DELETE
```


يعرض مراجعات الإدراج داخل السطر، ومراجعات الحذف والتنسيق في الفقاعات.

### NONE {#NONE}
```
public static int NONE
```


يعرض مراجعات الإدراج والحذف والتنسيق داخل السطر.

### length {#length}
```
public static int length
```


### fromName(String showInBalloonsName) {#fromName-java.lang.String}
```
public static int fromName(String showInBalloonsName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| showInBalloonsName | java.lang.String |  |

**Returns:**
int
### getName(int showInBalloons) {#getName-int}
```
public static String getName(int showInBalloons)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| showInBalloons | int |  |

**Returns:**
java.lang.String
