---
title: "RevisionTextEffect"
linktitle: "RevisionTextEffect"
second_title: "Aspose.Words pour Java"
description: "Permet de spécifier l’effet de décoration pour les révisions du texte du document en Java."
type: docs
weight: 585
url: /fr/java/com.aspose.words/revisiontexteffect/
---

**Inheritance:**
java.lang.Object
```
public class RevisionTextEffect
```

Permet de spécifier l'effet de décoration pour les révisions du texte du document.

 **Examples:** 

Montre comment modifier l’apparence des révisions.

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
## Champs

| Champ | Description |
| --- | --- |
| [BOLD](#BOLD) | Le contenu révisé est mis en gras et coloré. |
| [COLOR](#COLOR) | Le contenu révisé est uniquement surligné en couleur. |
| [DOUBLE_STRIKE_THROUGH](#DOUBLE-STRIKE-THROUGH) | Le contenu révisé est doublement barré et coloré. |
| [DOUBLE_UNDERLINE](#DOUBLE-UNDERLINE) | Le contenu révisé est doublement souligné et coloré. |
| [HIDDEN](#HIDDEN) | Le contenu révisé est masqué. |
| [ITALIC](#ITALIC) | Le contenu révisé est mis en italique et coloré. |
| [NONE](#NONE) | Aucun effet spécial n’est appliqué au contenu révisé. |
| [STRIKE_THROUGH](#STRIKE-THROUGH) | Le contenu révisé est barré et coloré. |
| [UNDERLINE](#UNDERLINE) | Le contenu révisé est souligné et coloré. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String revisionTextEffectName)](#fromName-java.lang.String) |  |
| [getName(int revisionTextEffect)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int revisionTextEffect)](#toString-int) |  |
### BOLD {#BOLD}
```
public static int BOLD
```


Le contenu révisé est mis en gras et coloré.

### COLOR {#COLOR}
```
public static int COLOR
```


Le contenu révisé est uniquement surligné en couleur.

### DOUBLE_STRIKE_THROUGH {#DOUBLE-STRIKE-THROUGH}
```
public static int DOUBLE_STRIKE_THROUGH
```


Le contenu révisé est doublement barré et coloré.

 **Remarks:** 

Ne fonctionne que pour [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION), [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE) et [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING) ('move from' type).

### DOUBLE_UNDERLINE {#DOUBLE-UNDERLINE}
```
public static int DOUBLE_UNDERLINE
```


Le contenu révisé est doublement souligné et coloré.

### HIDDEN {#HIDDEN}
```
public static int HIDDEN
```


Le contenu révisé est masqué.

 **Remarks:** 

Ne fonctionne que pour [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION) et [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING) ('move from' type).

### ITALIC {#ITALIC}
```
public static int ITALIC
```


Le contenu révisé est mis en italique et coloré.

### NONE {#NONE}
```
public static int NONE
```


Aucun effet spécial n’est appliqué au contenu révisé. Cela correspond à [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT).

### STRIKE_THROUGH {#STRIKE-THROUGH}
```
public static int STRIKE_THROUGH
```


Le contenu révisé est barré et coloré.

### UNDERLINE {#UNDERLINE}
```
public static int UNDERLINE
```


Le contenu révisé est souligné et coloré.

### length {#length}
```
public static int length
```


### fromName(String revisionTextEffectName) {#fromName-java.lang.String}
```
public static int fromName(String revisionTextEffectName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| revisionTextEffectName | java.lang.String |  |

**Returns:**
int
### getName(int revisionTextEffect) {#getName-int}
```
public static String getName(int revisionTextEffect)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| revisionTextEffect | int |  |

**Returns:**
java.lang.String
