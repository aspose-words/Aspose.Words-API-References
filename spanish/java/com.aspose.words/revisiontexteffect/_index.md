---
title: "RevisionTextEffect"
linktitle: "RevisionTextEffect"
second_title: "Aspose.Words para Java"
description: "Permite especificar el efecto de decoración para revisiones del texto del documento en Java."
type: docs
weight: 585
url: /es/java/com.aspose.words/revisiontexteffect/
---

**Inheritance:**
java.lang.Object
```
public class RevisionTextEffect
```

Permite especificar el efecto de decoración para las revisiones del texto del documento.

 **Examples:** 

Muestra cómo modificar la apariencia de las revisiones.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [BOLD](#BOLD) | El contenido revisado se muestra en negrita y con color. |
| [COLOR](#COLOR) | El contenido revisado se resalta solo con color. |
| [DOUBLE_STRIKE_THROUGH](#DOUBLE-STRIKE-THROUGH) | El contenido revisado tiene doble tachado y color. |
| [DOUBLE_UNDERLINE](#DOUBLE-UNDERLINE) | El contenido revisado tiene doble subrayado y color. |
| [HIDDEN](#HIDDEN) | El contenido revisado está oculto. |
| [ITALIC](#ITALIC) | El contenido revisado se muestra en cursiva y con color. |
| [NONE](#NONE) | El contenido revisado no tiene efectos especiales aplicados. |
| [STRIKE_THROUGH](#STRIKE-THROUGH) | El contenido revisado tiene tachado y color. |
| [UNDERLINE](#UNDERLINE) | El contenido revisado está subrayado y con color. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String revisionTextEffectName)](#fromName-java.lang.String) |  |
| [getName(int revisionTextEffect)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int revisionTextEffect)](#toString-int) |  |
### BOLD {#BOLD}
```
public static int BOLD
```


El contenido revisado se muestra en negrita y con color.

### COLOR {#COLOR}
```
public static int COLOR
```


El contenido revisado se resalta solo con color.

### DOUBLE_STRIKE_THROUGH {#DOUBLE-STRIKE-THROUGH}
```
public static int DOUBLE_STRIKE_THROUGH
```


El contenido revisado tiene doble tachado y color.

 **Remarks:** 

Solo funciona para [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION), [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE) y [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING) (tipo 'move from').

### DOUBLE_UNDERLINE {#DOUBLE-UNDERLINE}
```
public static int DOUBLE_UNDERLINE
```


El contenido revisado tiene doble subrayado y color.

### HIDDEN {#HIDDEN}
```
public static int HIDDEN
```


El contenido revisado está oculto.

 **Remarks:** 

Solo funciona para [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION) y [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING) (tipo 'move from').

### ITALIC {#ITALIC}
```
public static int ITALIC
```


El contenido revisado se muestra en cursiva y con color.

### NONE {#NONE}
```
public static int NONE
```


El contenido revisado no tiene efectos especiales aplicados. Esto corresponde a [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT).

### STRIKE_THROUGH {#STRIKE-THROUGH}
```
public static int STRIKE_THROUGH
```


El contenido revisado tiene tachado y color.

### UNDERLINE {#UNDERLINE}
```
public static int UNDERLINE
```


El contenido revisado está subrayado y con color.

### length {#length}
```
public static int length
```


### fromName(String revisionTextEffectName) {#fromName-java.lang.String}
```
public static int fromName(String revisionTextEffectName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| revisionTextEffectName | java.lang.String |  |

**Returns:**
int
### getName(int revisionTextEffect) {#getName-int}
```
public static String getName(int revisionTextEffect)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| revisionTextEffect | int |  |

**Returns:**
java.lang.String
