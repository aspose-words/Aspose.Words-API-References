---
title: "DocumentRecoveryMode"
linktitle: "DocumentRecoveryMode"
second_title: "Aspose.Words per Java"
description: "Specifica le opzioni di recupero disponibili quando un documento incontra errori durante il caricamento in Java."
type: docs
weight: 171
url: /it/java/com.aspose.words/documentrecoverymode/
---

**Inheritance:**
java.lang.Object
```
public class DocumentRecoveryMode
```

Specifica le opzioni di recupero disponibili quando un documento incontra errori durante il caricamento.

 **Examples:** 

Mostra come provare a recuperare un documento se si sono verificati errori durante il caricamento.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setRecoveryMode(DocumentRecoveryMode.TRY_RECOVER);

 Document doc = new Document(getMyDir() + "Corrupted footnotes.docx", loadOptions);
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [NONE](#NONE) | Non viene tentato alcun recupero. |
| [TRY_RECOVER](#TRY-RECOVER) | Tenta di recuperare il documento preservando il più possibile i dati. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String documentRecoveryModeName)](#fromName-java.lang.String) |  |
| [getName(int documentRecoveryMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int documentRecoveryMode)](#toString-int) |  |
### NONE {#NONE}
```
public static int NONE
```


Non viene tentato alcun recupero. Se il documento è non valido, il caricamento fallirà con un errore.

### TRY_RECOVER {#TRY-RECOVER}
```
public static int TRY_RECOVER
```


Tenta di recuperare il documento preservando il più possibile i dati.

### length {#length}
```
public static int length
```


### fromName(String documentRecoveryModeName) {#fromName-java.lang.String}
```
public static int fromName(String documentRecoveryModeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| documentRecoveryModeName | java.lang.String |  |

**Returns:**
int
### getName(int documentRecoveryMode) {#getName-int}
```
public static String getName(int documentRecoveryMode)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| documentRecoveryMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int documentRecoveryMode) {#toString-int}
```
public static String toString(int documentRecoveryMode)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| documentRecoveryMode | int |  |

**Returns:**
java.lang.String
