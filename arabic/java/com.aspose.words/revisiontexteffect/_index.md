---
title: "RevisionTextEffect"
linktitle: "RevisionTextEffect"
second_title: "Aspose.Words لـ Java"
description: "يسمح بتحديد تأثير الزخرفة لتعديلات نص المستند في Java."
type: docs
weight: 585
url: /ar/java/com.aspose.words/revisiontexteffect/
---

**Inheritance:**
java.lang.Object
```
public class RevisionTextEffect
```

يسمح بتحديد تأثير الزخرفة لمراجعات نص المستند.

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
| [BOLD](#BOLD) | يتم جعل المحتوى المعدل غامقًا وملونًا. |
| [COLOR](#COLOR) | يتم تمييز المحتوى المعدل باللون فقط. |
| [DOUBLE_STRIKE_THROUGH](#DOUBLE-STRIKE-THROUGH) | يتم شطب المحتوى المعدل بخط مزدوج وتلوينه. |
| [DOUBLE_UNDERLINE](#DOUBLE-UNDERLINE) | يتم وضع خط مزدوج أسفل المحتوى المعدل وتلوينه. |
| [HIDDEN](#HIDDEN) | المحتوى المعدل مخفي. |
| [ITALIC](#ITALIC) | يتم جعل المحتوى المعدل مائلًا وتلوينه. |
| [NONE](#NONE) | المحتوى المعدل لا يحتوي على أي تأثيرات خاصة مطبقة. |
| [STRIKE_THROUGH](#STRIKE-THROUGH) | يتم شطب المحتوى المعدل وتلوينه. |
| [UNDERLINE](#UNDERLINE) | يتم وضع خط تحت المحتوى المعدل وتلوينه. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String revisionTextEffectName)](#fromName-java.lang.String) |  |
| [getName(int revisionTextEffect)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int revisionTextEffect)](#toString-int) |  |
### BOLD {#BOLD}
```
public static int BOLD
```


يتم جعل المحتوى المعدل غامقًا وملونًا.

### COLOR {#COLOR}
```
public static int COLOR
```


يتم تمييز المحتوى المعدل باللون فقط.

### DOUBLE_STRIKE_THROUGH {#DOUBLE-STRIKE-THROUGH}
```
public static int DOUBLE_STRIKE_THROUGH
```


يتم شطب المحتوى المعدل بخط مزدوج وتلوينه.

 **Remarks:** 

يعمل فقط مع [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION)، [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE) و [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING) ('move from' type).

### DOUBLE_UNDERLINE {#DOUBLE-UNDERLINE}
```
public static int DOUBLE_UNDERLINE
```


يتم وضع خط مزدوج أسفل المحتوى المعدل وتلوينه.

### HIDDEN {#HIDDEN}
```
public static int HIDDEN
```


المحتوى المعدل مخفي.

 **Remarks:** 

يعمل فقط مع [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION) و [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING) ('move from' type).

### ITALIC {#ITALIC}
```
public static int ITALIC
```


يتم جعل المحتوى المعدل مائلًا وتلوينه.

### NONE {#NONE}
```
public static int NONE
```


المحتوى المعدل لا يحتوي على أي تأثيرات خاصة مطبقة. وهذا يتطابق مع [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT).

### STRIKE_THROUGH {#STRIKE-THROUGH}
```
public static int STRIKE_THROUGH
```


يتم شطب المحتوى المعدل وتلوينه.

### UNDERLINE {#UNDERLINE}
```
public static int UNDERLINE
```


يتم وضع خط تحت المحتوى المعدل وتلوينه.

### length {#length}
```
public static int length
```


### fromName(String revisionTextEffectName) {#fromName-java.lang.String}
```
public static int fromName(String revisionTextEffectName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| revisionTextEffectName | java.lang.String |  |

**Returns:**
int
### getName(int revisionTextEffect) {#getName-int}
```
public static String getName(int revisionTextEffect)
```




**Parameters:**
| معامل | نوع | الوصف |
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
### toString(int revisionTextEffect) {#toString-int}
```
public static String toString(int revisionTextEffect)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| revisionTextEffect | int |  |

**Returns:**
java.lang.String
