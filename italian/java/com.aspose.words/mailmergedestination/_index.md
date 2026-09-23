---
title: "MailMergeDestination"
linktitle: "MailMergeDestination"
second_title: "Aspose.Words per Java"
description: "Specifica i possibili risultati che possono essere generati quando viene eseguita una stampa unione su un documento in Java."
type: docs
weight: 441
url: /it/java/com.aspose.words/mailmergedestination/
---

**Inheritance:**
java.lang.Object
```
public class MailMergeDestination
```

Specifica i possibili risultati che possono essere generati quando una stampa unione viene eseguita su un documento.
## Campi

| Campo | Descrizione |
| --- | --- |
| [DEFAULT](#DEFAULT) | Uguale al valore [NEW\_DOCUMENT](../../com.aspose.words/mailmergedestination/\#NEW-DOCUMENT). |
| [EMAIL](#EMAIL) | Specifica che le applicazioni host conformi devono generare email utilizzando i documenti risultanti dal popolamento dei campi all'interno di un dato documento con i dati dalla fonte dati esterna specificata. |
| [FAX](#FAX) | Specifica che le applicazioni host conformi devono generare fax utilizzando i documenti risultanti dal popolamento dei campi all'interno di un dato documento con i dati dalla fonte dati esterna specificata. |
| [NEW_DOCUMENT](#NEW-DOCUMENT) | Specifica che le applicazioni host conformi devono generare nuovi documenti popolando i campi all'interno di un dato documento con i dati dalla fonte dati esterna specificata. |
| [PRINTER](#PRINTER) | Specifica che le applicazioni host conformi devono stampare i documenti risultanti dal popolamento dei campi all'interno di un dato documento con dati esterni dalla fonte dati esterna specificata. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String mailMergeDestinationName)](#fromName-java.lang.String) |  |
| [getName(int mailMergeDestination)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int mailMergeDestination)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Uguale al valore [NEW\_DOCUMENT](../../com.aspose.words/mailmergedestination/\#NEW-DOCUMENT).

### EMAIL {#EMAIL}
```
public static int EMAIL
```


Specifica che le applicazioni host conformi devono generare email utilizzando i documenti risultanti dal popolamento dei campi all'interno di un dato documento con i dati dalla fonte dati esterna specificata.

### FAX {#FAX}
```
public static int FAX
```


Specifica che le applicazioni host conformi devono generare fax utilizzando i documenti risultanti dal popolamento dei campi all'interno di un dato documento con i dati dalla fonte dati esterna specificata.

### NEW_DOCUMENT {#NEW-DOCUMENT}
```
public static int NEW_DOCUMENT
```


Specifica che le applicazioni host conformi devono generare nuovi documenti popolando i campi all'interno di un dato documento con i dati dalla fonte dati esterna specificata.

### PRINTER {#PRINTER}
```
public static int PRINTER
```


Specifica che le applicazioni host conformi devono stampare i documenti risultanti dal popolamento dei campi all'interno di un dato documento con dati esterni dalla fonte dati esterna specificata.

### length {#length}
```
public static int length
```


### fromName(String mailMergeDestinationName) {#fromName-java.lang.String}
```
public static int fromName(String mailMergeDestinationName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| mailMergeDestinationName | java.lang.String |  |

**Returns:**
int
### getName(int mailMergeDestination) {#getName-int}
```
public static String getName(int mailMergeDestination)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| mailMergeDestination | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int mailMergeDestination) {#toString-int}
```
public static String toString(int mailMergeDestination)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| mailMergeDestination | int |  |

**Returns:**
java.lang.String
