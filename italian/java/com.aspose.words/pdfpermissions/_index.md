---
title: "PdfPermissions"
linktitle: "PdfPermissions"
second_title: "Aspose.Words per Java"
description: "Specifica le operazioni consentite a un utente su un documento PDF crittografato in Java."
type: docs
weight: 541
url: /it/java/com.aspose.words/pdfpermissions/
---

**Inheritance:**
java.lang.Object
```
public class PdfPermissions
```

Specifica le operazioni consentite a un utente su un documento PDF crittografato.

 **Examples:** 

Mostra come impostare le autorizzazioni su un documento PDF salvato.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Extend permissions to allow the editing of annotations.
 PdfEncryptionDetails encryptionDetails =
         new PdfEncryptionDetails("password", "", PdfPermissions.MODIFY_ANNOTATIONS | PdfPermissions.DOCUMENT_ASSEMBLY);

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Enable encryption via the "EncryptionDetails" property.
 saveOptions.setEncryptionDetails(encryptionDetails);

 // When we open this document, we will need to provide the password before accessing its contents.
 doc.save(getArtifactsDir() + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [ALLOW_ALL](#ALLOW-ALL) | Consente tutte le operazioni sul documento PDF. |
| [CONTENT_COPY](#CONTENT-COPY) | Copia o estrae in altro modo testo e grafica dal documento mediante operazioni diverse da quelle controllate da [CONTENT\_COPY\_FOR\_ACCESSIBILITY](../../com.aspose.words/pdfpermissions/\#CONTENT-COPY-FOR-ACCESSIBILITY). |
| [CONTENT_COPY_FOR_ACCESSIBILITY](#CONTENT-COPY-FOR-ACCESSIBILITY) | Estrai testo e grafica (a supporto dell'accessibilità per utenti con disabilità o per altri scopi). |
| [DISALLOW_ALL](#DISALLOW-ALL) | Non consente alcuna operazione sul documento PDF. |
| [DOCUMENT_ASSEMBLY](#DOCUMENT-ASSEMBLY) | Assemblare il documento (inserire, ruotare o eliminare pagine e creare voci di struttura del documento o immagini in miniatura), anche se [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) è disattivato. |
| [FILL_IN](#FILL-IN) | Compila i campi di modulo interattivi esistenti (inclusi i campi firma), anche se [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) è disattivato. |
| [HIGH_RESOLUTION_PRINTING](#HIGH-RESOLUTION-PRINTING) | Stampa il documento in una rappresentazione da cui può essere generata una copia digitale fedele del contenuto PDF, basata su un algoritmo dipendente dall'implementazione. |
| [MODIFY_ANNOTATIONS](#MODIFY-ANNOTATIONS) | Aggiungi o modifica annotazioni di testo, compila i campi di modulo interattivi e, se [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) è anche impostato, crea o modifica campi di modulo interattivi (inclusi i campi firma). |
| [MODIFY_CONTENTS](#MODIFY-CONTENTS) | Modifica il contenuto del documento mediante operazioni diverse da quelle controllate da [MODIFY\_ANNOTATIONS](../../com.aspose.words/pdfpermissions/\#MODIFY-ANNOTATIONS), [FILL\_IN](../../com.aspose.words/pdfpermissions/\#FILL-IN) e [DOCUMENT\_ASSEMBLY](../../com.aspose.words/pdfpermissions/\#DOCUMENT-ASSEMBLY). |
| [PRINTING](#PRINTING) | Stampa il documento (potenzialmente non al massimo livello di qualità, a seconda se [HIGH\_RESOLUTION\_PRINTING](../../com.aspose.words/pdfpermissions/\#HIGH-RESOLUTION-PRINTING) è anche impostato). |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String pdfPermissionsName)](#fromName-java.lang.String) |  |
| [fromNames(Set pdfPermissionsNames)](#fromNames-java.util.Set) |  |
| [getName(int pdfPermissions)](#getName-int) |  |
| [getNames(int pdfPermissions)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfPermissions)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### ALLOW_ALL {#ALLOW-ALL}
```
public static int ALLOW_ALL
```


Consente tutte le operazioni sul documento PDF.

### CONTENT_COPY {#CONTENT-COPY}
```
public static int CONTENT_COPY
```


Copia o estrae in altro modo testo e grafica dal documento mediante operazioni diverse da quelle controllate da [CONTENT\_COPY\_FOR\_ACCESSIBILITY](../../com.aspose.words/pdfpermissions/\#CONTENT-COPY-FOR-ACCESSIBILITY).

### CONTENT_COPY_FOR_ACCESSIBILITY {#CONTENT-COPY-FOR-ACCESSIBILITY}
```
public static int CONTENT_COPY_FOR_ACCESSIBILITY
```


Estrai testo e grafica (a supporto dell'accessibilità per utenti con disabilità o per altri scopi).

### DISALLOW_ALL {#DISALLOW-ALL}
```
public static int DISALLOW_ALL
```


Non consente alcuna operazione sul documento PDF. Questo è il valore predefinito.

### DOCUMENT_ASSEMBLY {#DOCUMENT-ASSEMBLY}
```
public static int DOCUMENT_ASSEMBLY
```


Assemblare il documento (inserire, ruotare o eliminare pagine e creare voci di struttura del documento o immagini in miniatura), anche se [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) è disattivato.

### FILL_IN {#FILL-IN}
```
public static int FILL_IN
```


Compila i campi di modulo interattivi esistenti (inclusi i campi firma), anche se [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) è disattivato.

### HIGH_RESOLUTION_PRINTING {#HIGH-RESOLUTION-PRINTING}
```
public static int HIGH_RESOLUTION_PRINTING
```


Stampa il documento in una rappresentazione da cui può essere generata una copia digitale fedele del contenuto PDF, basata su un algoritmo dipendente dall'implementazione. Quando questo flag è disattivato (e [PRINTING](../../com.aspose.words/pdfpermissions/\#PRINTING) è impostato), la stampa deve essere limitata a una rappresentazione di basso livello dell'aspetto, possibilmente di qualità ridotta.

### MODIFY_ANNOTATIONS {#MODIFY-ANNOTATIONS}
```
public static int MODIFY_ANNOTATIONS
```


Aggiungi o modifica annotazioni di testo, compila i campi di modulo interattivi e, se [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) è anche impostato, crea o modifica campi di modulo interattivi (inclusi i campi firma).

### MODIFY_CONTENTS {#MODIFY-CONTENTS}
```
public static int MODIFY_CONTENTS
```


Modifica il contenuto del documento mediante operazioni diverse da quelle controllate da [MODIFY\_ANNOTATIONS](../../com.aspose.words/pdfpermissions/\#MODIFY-ANNOTATIONS), [FILL\_IN](../../com.aspose.words/pdfpermissions/\#FILL-IN) e [DOCUMENT\_ASSEMBLY](../../com.aspose.words/pdfpermissions/\#DOCUMENT-ASSEMBLY).

### PRINTING {#PRINTING}
```
public static int PRINTING
```


Stampa il documento (potenzialmente non al massimo livello di qualità, a seconda se [HIGH\_RESOLUTION\_PRINTING](../../com.aspose.words/pdfpermissions/\#HIGH-RESOLUTION-PRINTING) è anche impostato).

### length {#length}
```
public static int length
```


### fromName(String pdfPermissionsName) {#fromName-java.lang.String}
```
public static int fromName(String pdfPermissionsName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pdfPermissionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set pdfPermissionsNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set pdfPermissionsNames)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pdfPermissionsNames | java.util.Set |  |

**Returns:**
int
### getName(int pdfPermissions) {#getName-int}
```
public static String getName(int pdfPermissions)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pdfPermissions | int |  |

**Returns:**
java.lang.String
### getNames(int pdfPermissions) {#getNames-int}
```
public static Set getNames(int pdfPermissions)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pdfPermissions | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pdfPermissions) {#toString-int}
```
public static String toString(int pdfPermissions)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pdfPermissions | int |  |

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
