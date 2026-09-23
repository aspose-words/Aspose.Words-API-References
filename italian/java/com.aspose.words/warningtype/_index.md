---
title: "WarningType"
linktitle: "WarningType"
second_title: "Aspose.Words per Java"
description: "Specifica il tipo di avviso emesso da Aspose.Words durante il caricamento o il salvataggio del documento in Java."
type: docs
weight: 720
url: /it/java/com.aspose.words/warningtype/
---

**Inheritance:**
java.lang.Object
```
public class WarningType
```

Specifica il tipo di avviso emesso da **Aspose.Words** durante il caricamento o il salvataggio del documento.

 **Examples:** 

Mostra come impostare la proprietà per trovare la corrispondenza più vicina per un carattere mancante dalle font disponibili.

```

 // Open a document that contains text formatted with a font that does not exist in any of our font sources.
 Document doc = new Document(getMyDir() + "Missing font.docx");

 // Assign a callback for handling font substitution warnings.
 WarningInfoCollection warningCollector = new WarningInfoCollection();
 doc.setWarningCallback(warningCollector);

 // Set a default font name and enable font substitution.
 FontSettings fontSettings = new FontSettings();
 fontSettings.getSubstitutionSettings().getDefaultFontSubstitution().setDefaultFontName("Arial");
 fontSettings.getSubstitutionSettings().getFontInfoSubstitution().setEnabled(true);

 // Original font metrics should be used after font substitution.
 doc.getLayoutOptions().setKeepOriginalFontMetrics(true);

 // We will get a font substitution warning if we save a document with a missing font.
 doc.setFontSettings(fontSettings);
 doc.save(getArtifactsDir() + "FontSettings.EnableFontSubstitution.pdf");

 for (WarningInfo info : warningCollector)
 {
     if (info.getWarningType() == WarningType.FONT_SUBSTITUTION)
         System.out.println(info.getDescription());
 }
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [DATA_LOSS](#DATA-LOSS) | Perdita di dati generica, nessun codice specifico. |
| [DATA_LOSS_CATEGORY](#DATA-LOSS-CATEGORY) | Alcuni testo/carattere/immagine o altri dati mancheranno sia dall'albero del documento dopo il caricamento, sia dal documento creato dopo il salvataggio. |
| [FONT_EMBEDDING](#FONT-EMBEDDING) | Perdita delle informazioni dei font incorporati durante il salvataggio del documento. |
| [FONT_SUBSTITUTION](#FONT-SUBSTITUTION) | Il font è stato sostituito. |
| [HINT](#HINT) | Avverte di un potenziale problema o suggerisce un miglioramento. |
| [MAJOR_FORMATTING_LOSS](#MAJOR-FORMATTING-LOSS) | Perdita di formattazione maggiore generica, nessun codice specifico. |
| [MAJOR_FORMATTING_LOSS_CATEGORY](#MAJOR-FORMATTING-LOSS-CATEGORY) | Il documento risultante o una sua posizione particolare potrebbe apparire sostanzialmente diversa rispetto al documento originale. |
| [MINOR_FORMATTING_LOSS](#MINOR-FORMATTING-LOSS) | Perdita di formattazione minore generica, nessun codice specifico. |
| [MINOR_FORMATTING_LOSS_CATEGORY](#MINOR-FORMATTING-LOSS-CATEGORY) | Il documento risultante o una sua posizione particolare potrebbe apparire leggermente diversa rispetto al documento originale. |
| [UNEXPECTED_CONTENT](#UNEXPECTED-CONTENT) | Contenuto inaspettato generico, nessun codice specifico. |
| [UNEXPECTED_CONTENT_CATEGORY](#UNEXPECTED-CONTENT-CATEGORY) | Alcuni contenuti nel documento sorgente non sono stati riconosciuti (ad esempio. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String warningTypeName)](#fromName-java.lang.String) |  |
| [fromNames(Set warningTypeNames)](#fromNames-java.util.Set) |  |
| [getName(int warningType)](#getName-int) |  |
| [getNames(int warningType)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int warningType)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### DATA_LOSS {#DATA-LOSS}
```
public static int DATA_LOSS
```


Perdita di dati generica, nessun codice specifico.

### DATA_LOSS_CATEGORY {#DATA-LOSS-CATEGORY}
```
public static int DATA_LOSS_CATEGORY
```


Alcuni testo/carattere/immagine o altri dati mancheranno sia dall'albero del documento dopo il caricamento, sia dal documento creato dopo il salvataggio.

### FONT_EMBEDDING {#FONT-EMBEDDING}
```
public static int FONT_EMBEDDING
```


Perdita delle informazioni dei font incorporati durante il salvataggio del documento.

### FONT_SUBSTITUTION {#FONT-SUBSTITUTION}
```
public static int FONT_SUBSTITUTION
```


Il font è stato sostituito.

### HINT {#HINT}
```
public static int HINT
```


Avverte di un potenziale problema o suggerisce un miglioramento.

### MAJOR_FORMATTING_LOSS {#MAJOR-FORMATTING-LOSS}
```
public static int MAJOR_FORMATTING_LOSS
```


Perdita di formattazione maggiore generica, nessun codice specifico.

### MAJOR_FORMATTING_LOSS_CATEGORY {#MAJOR-FORMATTING-LOSS-CATEGORY}
```
public static int MAJOR_FORMATTING_LOSS_CATEGORY
```


Il documento risultante o una sua posizione particolare potrebbe apparire sostanzialmente diversa rispetto al documento originale.

### MINOR_FORMATTING_LOSS {#MINOR-FORMATTING-LOSS}
```
public static int MINOR_FORMATTING_LOSS
```


Perdita di formattazione minore generica, nessun codice specifico.

### MINOR_FORMATTING_LOSS_CATEGORY {#MINOR-FORMATTING-LOSS-CATEGORY}
```
public static int MINOR_FORMATTING_LOSS_CATEGORY
```


Il documento risultante o una sua posizione particolare potrebbe apparire leggermente diversa rispetto al documento originale.

### UNEXPECTED_CONTENT {#UNEXPECTED-CONTENT}
```
public static int UNEXPECTED_CONTENT
```


Contenuto inaspettato generico, nessun codice specifico.

### UNEXPECTED_CONTENT_CATEGORY {#UNEXPECTED-CONTENT-CATEGORY}
```
public static int UNEXPECTED_CONTENT_CATEGORY
```


Alcuni contenuti nel documento sorgente non sono stati riconosciuti (ad esempio non sono supportati), questo potrebbe o meno causare problemi o provocare perdita di dati/formattazione.

### length {#length}
```
public static int length
```


### fromName(String warningTypeName) {#fromName-java.lang.String}
```
public static int fromName(String warningTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| warningTypeName | java.lang.String |  |

**Returns:**
int
### fromNames(Set warningTypeNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set warningTypeNames)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| warningTypeNames | java.util.Set |  |

**Returns:**
int
### getName(int warningType) {#getName-int}
```
public static String getName(int warningType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| warningType | int |  |

**Returns:**
java.lang.String
### getNames(int warningType) {#getNames-int}
```
public static Set getNames(int warningType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| warningType | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int warningType) {#toString-int}
```
public static String toString(int warningType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| warningType | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
