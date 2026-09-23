---
title: "RevisionTextEffect"
linktitle: "RevisionTextEffect"
second_title: "Aspose.Words per Java"
description: "Consente di specificare l'effetto di decorazione per le revisioni del testo del documento in Java."
type: docs
weight: 585
url: /it/java/com.aspose.words/revisiontexteffect/
---

**Inheritance:**
java.lang.Object
```
public class RevisionTextEffect
```

Consente di specificare l'effetto di decorazione per le revisioni del testo del documento.

 **Examples:** 

Mostra come modificare l'aspetto delle revisioni.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [BOLD](#BOLD) | Il contenuto revisionato è reso grassetto e colorato. |
| [COLOR](#COLOR) | Il contenuto revisionato è evidenziato solo con colore. |
| [DOUBLE_STRIKE_THROUGH](#DOUBLE-STRIKE-THROUGH) | Il contenuto revisionato è barrato due volte e colorato. |
| [DOUBLE_UNDERLINE](#DOUBLE-UNDERLINE) | Il contenuto revisionato è doppiamente sottolineato e colorato. |
| [HIDDEN](#HIDDEN) | Il contenuto revisionato è nascosto. |
| [ITALIC](#ITALIC) | Il contenuto revisionato è reso corsivo e colorato. |
| [NONE](#NONE) | Il contenuto revisionato non ha effetti speciali applicati. |
| [STRIKE_THROUGH](#STRIKE-THROUGH) | Il contenuto revisionato è barrato e colorato. |
| [UNDERLINE](#UNDERLINE) | Il contenuto revisionato è sottolineato e colorato. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String revisionTextEffectName)](#fromName-java.lang.String) |  |
| [getName(int revisionTextEffect)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int revisionTextEffect)](#toString-int) |  |
### BOLD {#BOLD}
```
public static int BOLD
```


Il contenuto revisionato è reso grassetto e colorato.

### COLOR {#COLOR}
```
public static int COLOR
```


Il contenuto revisionato è evidenziato solo con colore.

### DOUBLE_STRIKE_THROUGH {#DOUBLE-STRIKE-THROUGH}
```
public static int DOUBLE_STRIKE_THROUGH
```


Il contenuto revisionato è barrato due volte e colorato.

 **Remarks:** 

Funziona solo per [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION), [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE) e [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING) ('move from' type).

### DOUBLE_UNDERLINE {#DOUBLE-UNDERLINE}
```
public static int DOUBLE_UNDERLINE
```


Il contenuto revisionato è doppiamente sottolineato e colorato.

### HIDDEN {#HIDDEN}
```
public static int HIDDEN
```


Il contenuto revisionato è nascosto.

 **Remarks:** 

Funziona solo per [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION) e [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING) ('move from' type).

### ITALIC {#ITALIC}
```
public static int ITALIC
```


Il contenuto revisionato è reso corsivo e colorato.

### NONE {#NONE}
```
public static int NONE
```


Il contenuto revisionato non ha effetti speciali applicati. Questo corrisponde a [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT).

### STRIKE_THROUGH {#STRIKE-THROUGH}
```
public static int STRIKE_THROUGH
```


Il contenuto revisionato è barrato e colorato.

### UNDERLINE {#UNDERLINE}
```
public static int UNDERLINE
```


Il contenuto revisionato è sottolineato e colorato.

### length {#length}
```
public static int length
```


### fromName(String revisionTextEffectName) {#fromName-java.lang.String}
```
public static int fromName(String revisionTextEffectName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| revisionTextEffectName | java.lang.String |  |

**Returns:**
int
### getName(int revisionTextEffect) {#getName-int}
```
public static String getName(int revisionTextEffect)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| revisionTextEffect | int |  |

**Returns:**
java.lang.String
