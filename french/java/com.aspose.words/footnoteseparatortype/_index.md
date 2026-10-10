---
title: "FootnoteSeparatorType"
linktitle: "FootnoteSeparatorType"
second_title: "Aspose.Words pour Java"
description: "Spécifie le type du séparateur de note de bas de page/fin de note en Java."
type: docs
weight: 345
url: /fr/java/com.aspose.words/footnoteseparatortype/
---

**Inheritance:**
java.lang.Object
```
public class FootnoteSeparatorType
```

Spécifie le type du séparateur de note de bas de page/de note de fin.

 **Examples:** 

Montre comment supprimer le séparateur de fin de note.

```

 Document doc = new Document(getMyDir() + "Footnotes and endnotes.docx");

 FootnoteSeparator endnoteSeparator = doc.getFootnoteSeparators().getByFootnoteSeparatorType(FootnoteSeparatorType.ENDNOTE_SEPARATOR);
 // Remove endnote separator.
 endnoteSeparator.getFirstParagraph().getFirstChild().remove();
 
```

Montre comment gérer le format du séparateur de note de bas de page.

```

 Document doc = new Document(getMyDir() + "Footnotes and endnotes.docx");

 FootnoteSeparator footnoteSeparator = doc.getFootnoteSeparators().getByFootnoteSeparatorType(FootnoteSeparatorType.FOOTNOTE_SEPARATOR);
 // Align footnote separator.
 footnoteSeparator.getFirstParagraph().getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 
```
## Champs

| Champ | Description |
| --- | --- |
| [ENDNOTE_CONTINUATION_NOTICE](#ENDNOTE-CONTINUATION-NOTICE) | Imprimé sous le texte de la fin de note sur une page lorsque le texte de la fin de note doit être poursuivi sur la page suivante. |
| [ENDNOTE_CONTINUATION_SEPARATOR](#ENDNOTE-CONTINUATION-SEPARATOR) | Imprimé au-dessus du texte de la fin de note sur une page lorsque le texte doit être poursuivi depuis la page précédente. |
| [ENDNOTE_SEPARATOR](#ENDNOTE-SEPARATOR) | Séparateur entre le texte principal et le texte de la fin de note. |
| [FOOTNOTE_CONTINUATION_NOTICE](#FOOTNOTE-CONTINUATION-NOTICE) | Imprimé sous le texte de la note de bas de page sur une page lorsque le texte de la note de bas de page doit être poursuivi sur la page suivante. |
| [FOOTNOTE_CONTINUATION_SEPARATOR](#FOOTNOTE-CONTINUATION-SEPARATOR) | Imprimé au-dessus du texte de la note de bas de page sur une page lorsque le texte doit être poursuivi depuis la page précédente. |
| [FOOTNOTE_SEPARATOR](#FOOTNOTE-SEPARATOR) | Séparateur entre le texte principal et le texte de la note de bas de page. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String footnoteSeparatorTypeName)](#fromName-java.lang.String) |  |
| [getName(int footnoteSeparatorType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int footnoteSeparatorType)](#toString-int) |  |
### ENDNOTE_CONTINUATION_NOTICE {#ENDNOTE-CONTINUATION-NOTICE}
```
public static int ENDNOTE_CONTINUATION_NOTICE
```


Imprimé sous le texte de la fin de note sur une page lorsque le texte de la fin de note doit être poursuivi sur la page suivante.

### ENDNOTE_CONTINUATION_SEPARATOR {#ENDNOTE-CONTINUATION-SEPARATOR}
```
public static int ENDNOTE_CONTINUATION_SEPARATOR
```


Imprimé au-dessus du texte de la fin de note sur une page lorsque le texte doit être poursuivi depuis la page précédente.

### ENDNOTE_SEPARATOR {#ENDNOTE-SEPARATOR}
```
public static int ENDNOTE_SEPARATOR
```


Séparateur entre le texte principal et le texte de la fin de note.

### FOOTNOTE_CONTINUATION_NOTICE {#FOOTNOTE-CONTINUATION-NOTICE}
```
public static int FOOTNOTE_CONTINUATION_NOTICE
```


Imprimé sous le texte de la note de bas de page sur une page lorsque le texte de la note de bas de page doit être poursuivi sur la page suivante.

### FOOTNOTE_CONTINUATION_SEPARATOR {#FOOTNOTE-CONTINUATION-SEPARATOR}
```
public static int FOOTNOTE_CONTINUATION_SEPARATOR
```


Imprimé au-dessus du texte de la note de bas de page sur une page lorsque le texte doit être poursuivi depuis la page précédente.

### FOOTNOTE_SEPARATOR {#FOOTNOTE-SEPARATOR}
```
public static int FOOTNOTE_SEPARATOR
```


Séparateur entre le texte principal et le texte de la note de bas de page.

### length {#length}
```
public static int length
```


### fromName(String footnoteSeparatorTypeName) {#fromName-java.lang.String}
```
public static int fromName(String footnoteSeparatorTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| footnoteSeparatorTypeName | java.lang.String |  |

**Returns:**
int
### getName(int footnoteSeparatorType) {#getName-int}
```
public static String getName(int footnoteSeparatorType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| footnoteSeparatorType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int footnoteSeparatorType) {#toString-int}
```
public static String toString(int footnoteSeparatorType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| footnoteSeparatorType | int |  |

**Returns:**
java.lang.String
