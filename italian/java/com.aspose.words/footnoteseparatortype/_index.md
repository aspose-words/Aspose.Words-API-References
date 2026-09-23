---
title: "FootnoteSeparatorType"
linktitle: "FootnoteSeparatorType"
second_title: "Aspose.Words per Java"
description: "Specifica il tipo del separatore di nota a piè di pagina/note di chiusura in Java."
type: docs
weight: 345
url: /it/java/com.aspose.words/footnoteseparatortype/
---

**Inheritance:**
java.lang.Object
```
public class FootnoteSeparatorType
```

Specifica il tipo del separatore di nota a piè di pagina/fine nota.

 **Examples:** 

Mostra come rimuovere il separatore di nota di chiusura.

```

 Document doc = new Document(getMyDir() + "Footnotes and endnotes.docx");

 FootnoteSeparator endnoteSeparator = doc.getFootnoteSeparators().getByFootnoteSeparatorType(FootnoteSeparatorType.ENDNOTE_SEPARATOR);
 // Remove endnote separator.
 endnoteSeparator.getFirstParagraph().getFirstChild().remove();
 
```

Mostra come gestire il formato del separatore di nota a piè di pagina.

```

 Document doc = new Document(getMyDir() + "Footnotes and endnotes.docx");

 FootnoteSeparator footnoteSeparator = doc.getFootnoteSeparators().getByFootnoteSeparatorType(FootnoteSeparatorType.FOOTNOTE_SEPARATOR);
 // Align footnote separator.
 footnoteSeparator.getFirstParagraph().getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [ENDNOTE_CONTINUATION_NOTICE](#ENDNOTE-CONTINUATION-NOTICE) | Stampato sotto il testo della nota di chiusura su una pagina quando il testo della nota di chiusura deve essere continuato su una pagina successiva. |
| [ENDNOTE_CONTINUATION_SEPARATOR](#ENDNOTE-CONTINUATION-SEPARATOR) | Stampato sopra il testo della nota di chiusura su una pagina quando il testo deve essere continuato da una pagina precedente. |
| [ENDNOTE_SEPARATOR](#ENDNOTE-SEPARATOR) | Separatore tra il testo principale e il testo della nota di chiusura. |
| [FOOTNOTE_CONTINUATION_NOTICE](#FOOTNOTE-CONTINUATION-NOTICE) | Stampato sotto il testo della nota a piè di pagina su una pagina quando il testo della nota a piè di pagina deve essere continuato su una pagina successiva. |
| [FOOTNOTE_CONTINUATION_SEPARATOR](#FOOTNOTE-CONTINUATION-SEPARATOR) | Stampato sopra il testo della nota a piè di pagina su una pagina quando il testo deve essere continuato da una pagina precedente. |
| [FOOTNOTE_SEPARATOR](#FOOTNOTE-SEPARATOR) | Separatore tra il testo principale e il testo della nota a piè di pagina. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String footnoteSeparatorTypeName)](#fromName-java.lang.String) |  |
| [getName(int footnoteSeparatorType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int footnoteSeparatorType)](#toString-int) |  |
### ENDNOTE_CONTINUATION_NOTICE {#ENDNOTE-CONTINUATION-NOTICE}
```
public static int ENDNOTE_CONTINUATION_NOTICE
```


Stampato sotto il testo della nota di chiusura su una pagina quando il testo della nota di chiusura deve essere continuato su una pagina successiva.

### ENDNOTE_CONTINUATION_SEPARATOR {#ENDNOTE-CONTINUATION-SEPARATOR}
```
public static int ENDNOTE_CONTINUATION_SEPARATOR
```


Stampato sopra il testo della nota di chiusura su una pagina quando il testo deve essere continuato da una pagina precedente.

### ENDNOTE_SEPARATOR {#ENDNOTE-SEPARATOR}
```
public static int ENDNOTE_SEPARATOR
```


Separatore tra il testo principale e il testo della nota di chiusura.

### FOOTNOTE_CONTINUATION_NOTICE {#FOOTNOTE-CONTINUATION-NOTICE}
```
public static int FOOTNOTE_CONTINUATION_NOTICE
```


Stampato sotto il testo della nota a piè di pagina su una pagina quando il testo della nota a piè di pagina deve essere continuato su una pagina successiva.

### FOOTNOTE_CONTINUATION_SEPARATOR {#FOOTNOTE-CONTINUATION-SEPARATOR}
```
public static int FOOTNOTE_CONTINUATION_SEPARATOR
```


Stampato sopra il testo della nota a piè di pagina su una pagina quando il testo deve essere continuato da una pagina precedente.

### FOOTNOTE_SEPARATOR {#FOOTNOTE-SEPARATOR}
```
public static int FOOTNOTE_SEPARATOR
```


Separatore tra il testo principale e il testo della nota a piè di pagina.

### length {#length}
```
public static int length
```


### fromName(String footnoteSeparatorTypeName) {#fromName-java.lang.String}
```
public static int fromName(String footnoteSeparatorTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| footnoteSeparatorTypeName | java.lang.String |  |

**Returns:**
int
### getName(int footnoteSeparatorType) {#getName-int}
```
public static String getName(int footnoteSeparatorType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| footnoteSeparatorType | int |  |

**Returns:**
java.lang.String
