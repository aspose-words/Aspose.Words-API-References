---
title: "RevisionTextEffect"
linktitle: "RevisionTextEffect"
second_title: "Aspose.Words für Java"
description: "Ermöglicht das Festlegen von Dekorationseffekten für Revisionen von Dokumenttext in Java."
type: docs
weight: 585
url: /de/java/com.aspose.words/revisiontexteffect/
---

**Inheritance:**
java.lang.Object
```
public class RevisionTextEffect
```

Ermöglicht die Angabe eines Dekorationseffekts für Revisionen von Dokumenttext.

 **Examples:** 

Zeigt, wie das Erscheinungsbild von Revisionen geändert werden kann.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [BOLD](#BOLD) | Der überarbeitete Inhalt wird fett und farbig dargestellt. |
| [COLOR](#COLOR) | Der überarbeitete Inhalt wird nur mit Farbe hervorgehoben. |
| [DOUBLE_STRIKE_THROUGH](#DOUBLE-STRIKE-THROUGH) | Der überarbeitete Inhalt wird doppelt durchgestrichen und farbig dargestellt. |
| [DOUBLE_UNDERLINE](#DOUBLE-UNDERLINE) | Der überarbeitete Inhalt wird doppelt unterstrichen und farbig dargestellt. |
| [HIDDEN](#HIDDEN) | Der überarbeitete Inhalt wird ausgeblendet. |
| [ITALIC](#ITALIC) | Der überarbeitete Inhalt wird kursiv und farbig dargestellt. |
| [NONE](#NONE) | Auf den überarbeiteten Inhalt werden keine speziellen Effekte angewendet. |
| [STRIKE_THROUGH](#STRIKE-THROUGH) | Der überarbeitete Inhalt wird durchgestrichen und farbig dargestellt. |
| [UNDERLINE](#UNDERLINE) | Der überarbeitete Inhalt wird unterstrichen und farbig dargestellt. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String revisionTextEffectName)](#fromName-java.lang.String) |  |
| [getName(int revisionTextEffect)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int revisionTextEffect)](#toString-int) |  |
### BOLD {#BOLD}
```
public static int BOLD
```


Der überarbeitete Inhalt wird fett und farbig dargestellt.

### COLOR {#COLOR}
```
public static int COLOR
```


Der überarbeitete Inhalt wird nur mit Farbe hervorgehoben.

### DOUBLE_STRIKE_THROUGH {#DOUBLE-STRIKE-THROUGH}
```
public static int DOUBLE_STRIKE_THROUGH
```


Der überarbeitete Inhalt wird doppelt durchgestrichen und farbig dargestellt.

 **Remarks:** 

Funktioniert nur für [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION), [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE) und [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING) (Typ „move from“).

### DOUBLE_UNDERLINE {#DOUBLE-UNDERLINE}
```
public static int DOUBLE_UNDERLINE
```


Der überarbeitete Inhalt wird doppelt unterstrichen und farbig dargestellt.

### HIDDEN {#HIDDEN}
```
public static int HIDDEN
```


Der überarbeitete Inhalt wird ausgeblendet.

 **Remarks:** 

Funktioniert nur für [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION) und [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING) (Typ „move from“).

### ITALIC {#ITALIC}
```
public static int ITALIC
```


Der überarbeitete Inhalt wird kursiv und farbig dargestellt.

### NONE {#NONE}
```
public static int NONE
```


Auf den überarbeiteten Inhalt werden keine speziellen Effekte angewendet. Dies entspricht [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT).

### STRIKE_THROUGH {#STRIKE-THROUGH}
```
public static int STRIKE_THROUGH
```


Der überarbeitete Inhalt wird durchgestrichen und farbig dargestellt.

### UNDERLINE {#UNDERLINE}
```
public static int UNDERLINE
```


Der überarbeitete Inhalt wird unterstrichen und farbig dargestellt.

### length {#length}
```
public static int length
```


### fromName(String revisionTextEffectName) {#fromName-java.lang.String}
```
public static int fromName(String revisionTextEffectName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| revisionTextEffectName | java.lang.String |  |

**Returns:**
int
### getName(int revisionTextEffect) {#getName-int}
```
public static String getName(int revisionTextEffect)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| revisionTextEffect | int |  |

**Returns:**
java.lang.String
