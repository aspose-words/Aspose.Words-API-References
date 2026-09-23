---
title: "RevisionTextEffect"
linktitle: "RevisionTextEffect"
second_title: "Aspose.Words для Java"
description: "Позволяет указать эффект декорирования для исправлений текста документа в Java."
type: docs
weight: 585
url: /ru/java/com.aspose.words/revisiontexteffect/
---

**Inheritance:**
java.lang.Object
```
public class RevisionTextEffect
```

Позволяет указать эффект декорирования для ревизий текста документа.

 **Examples:** 

Показывает, как изменить внешний вид исправлений.

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
## Поля

| Поле | Описание |
| --- | --- |
| [BOLD](#BOLD) | Изменённый контент делается полужирным и окрашивается. |
| [COLOR](#COLOR) | Изменённый контент выделяется только цветом. |
| [DOUBLE_STRIKE_THROUGH](#DOUBLE-STRIKE-THROUGH) | Изменённый контент имеет двойное зачеркивание и окрашен. |
| [DOUBLE_UNDERLINE](#DOUBLE-UNDERLINE) | Изменённый контент имеет двойное подчёркивание и окрашен. |
| [HIDDEN](#HIDDEN) | Изменённый контент скрыт. |
| [ITALIC](#ITALIC) | Изменённый контент делается курсивом и окрашен. |
| [NONE](#NONE) | К изменённому контенту не применяются специальные эффекты. |
| [STRIKE_THROUGH](#STRIKE-THROUGH) | Изменённый контент зачеркивается и окрашен. |
| [UNDERLINE](#UNDERLINE) | Изменённый контент подчёркнут и окрашен. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String revisionTextEffectName)](#fromName-java.lang.String) |  |
| [getName(int revisionTextEffect)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int revisionTextEffect)](#toString-int) |  |
### BOLD {#BOLD}
```
public static int BOLD
```


Изменённый контент делается полужирным и окрашивается.

### COLOR {#COLOR}
```
public static int COLOR
```


Изменённый контент выделяется только цветом.

### DOUBLE_STRIKE_THROUGH {#DOUBLE-STRIKE-THROUGH}
```
public static int DOUBLE_STRIKE_THROUGH
```


Изменённый контент имеет двойное зачеркивание и окрашен.

 **Remarks:** 

Работает только для [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION), [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE) и [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING) (тип «перемещение из»).

### DOUBLE_UNDERLINE {#DOUBLE-UNDERLINE}
```
public static int DOUBLE_UNDERLINE
```


Изменённый контент имеет двойное подчёркивание и окрашен.

### HIDDEN {#HIDDEN}
```
public static int HIDDEN
```


Изменённый контент скрыт.

 **Remarks:** 

Работает только для [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION) и [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING) (тип «перемещение из»).

### ITALIC {#ITALIC}
```
public static int ITALIC
```


Изменённый контент делается курсивом и окрашен.

### NONE {#NONE}
```
public static int NONE
```


К изменённому контенту не применяются специальные эффекты. Это соответствует [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT).

### STRIKE_THROUGH {#STRIKE-THROUGH}
```
public static int STRIKE_THROUGH
```


Изменённый контент зачеркивается и окрашен.

### UNDERLINE {#UNDERLINE}
```
public static int UNDERLINE
```


Изменённый контент подчёркнут и окрашен.

### length {#length}
```
public static int length
```


### fromName(String revisionTextEffectName) {#fromName-java.lang.String}
```
public static int fromName(String revisionTextEffectName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| revisionTextEffectName | java.lang.String |  |

**Returns:**
int
### getName(int revisionTextEffect) {#getName-int}
```
public static String getName(int revisionTextEffect)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| revisionTextEffect | int |  |

**Returns:**
java.lang.String
