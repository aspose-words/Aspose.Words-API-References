---
title: "RevisionTextEffect"
linktitle: "RevisionTextEffect"
second_title: "Aspose.Words Java için"
description: "Java'da belge metni revizyonları için süsleme etkisini belirtmeye izin verir."
type: docs
weight: 585
url: /tr/java/com.aspose.words/revisiontexteffect/
---

**Inheritance:**
java.lang.Object
```
public class RevisionTextEffect
```

Belge metni revizyonları için süsleme etkisini belirtmeye olanak tanır.

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
| [BOLD](#BOLD) | Revize edilen içerik kalın ve renkli yapılır. |
| [COLOR](#COLOR) | Revize edilen içerik sadece renk ile vurgulanır. |
| [DOUBLE_STRIKE_THROUGH](#DOUBLE-STRIKE-THROUGH) | Revize edilen içerik iki kez üstü çizili ve renkli olur. |
| [DOUBLE_UNDERLINE](#DOUBLE-UNDERLINE) | Revize edilen içerik iki kez altı çizili ve renkli olur. |
| [HIDDEN](#HIDDEN) | Revize edilen içerik gizlidir. |
| [ITALIC](#ITALIC) | Revize edilen içerik italik ve renkli yapılır. |
| [NONE](#NONE) | Revize edilen içerik hiçbir özel etki uygulanmaz. |
| [STRIKE_THROUGH](#STRIKE-THROUGH) | Revize edilen içerik üstü çizili ve renkli olur. |
| [UNDERLINE](#UNDERLINE) | Revize edilen içerik altı çizili ve renkli olur. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String revisionTextEffectName)](#fromName-java.lang.String) |  |
| [getName(int revisionTextEffect)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int revisionTextEffect)](#toString-int) |  |
### BOLD {#BOLD}
```
public static int BOLD
```


Revize edilen içerik kalın ve renkli yapılır.

### COLOR {#COLOR}
```
public static int COLOR
```


Revize edilen içerik sadece renk ile vurgulanır.

### DOUBLE_STRIKE_THROUGH {#DOUBLE-STRIKE-THROUGH}
```
public static int DOUBLE_STRIKE_THROUGH
```


Revize edilen içerik iki kez üstü çizili ve renkli olur.

 **Remarks:** 

Yalnızca [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION), [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE) ve [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING) ('move from' türü) için çalışır.

### DOUBLE_UNDERLINE {#DOUBLE-UNDERLINE}
```
public static int DOUBLE_UNDERLINE
```


Revize edilen içerik iki kez altı çizili ve renkli olur.

### HIDDEN {#HIDDEN}
```
public static int HIDDEN
```


Revize edilen içerik gizlidir.

 **Remarks:** 

Yalnızca [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION) ve [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING) ('move from' türü) için çalışır.

### ITALIC {#ITALIC}
```
public static int ITALIC
```


Revize edilen içerik italik ve renkli yapılır.

### NONE {#NONE}
```
public static int NONE
```


Revize edilen içerik hiçbir özel etki uygulanmaz. Bu, [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT) ile eşdeğerdir.

### STRIKE_THROUGH {#STRIKE-THROUGH}
```
public static int STRIKE_THROUGH
```


Revize edilen içerik üstü çizili ve renkli olur.

### UNDERLINE {#UNDERLINE}
```
public static int UNDERLINE
```


Revize edilen içerik altı çizili ve renkli olur.

### length {#length}
```
public static int length
```


### fromName(String revisionTextEffectName) {#fromName-java.lang.String}
```
public static int fromName(String revisionTextEffectName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| revisionTextEffectName | java.lang.String |  |

**Returns:**
int
### getName(int revisionTextEffect) {#getName-int}
```
public static String getName(int revisionTextEffect)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| revisionTextEffect | int |  |

**Returns:**
java.lang.String
