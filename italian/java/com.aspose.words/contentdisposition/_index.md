---
title: "ContentDisposition"
linktitle: "ContentDisposition"
second_title: "Aspose.Words per Java"
description: "Elenca i diversi modi di presentare il documento nel browser client in Java."
type: docs
weight: 126
url: /it/java/com.aspose.words/contentdisposition/
---

**Inheritance:**
java.lang.Object
```
public class ContentDisposition
```

Enumera i diversi modi di presentare il documento nel browser client.

 **Remarks:** 

Nota che il comportamento effettivo nel browser client potrebbe essere influenzato dalla configurazione di sicurezza del browser.

 **Examples:** 

Mostra come eseguire un'unione di stampa e quindi salvare il documento nel browser client.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertField(" MERGEFIELD FullName ");
 builder.insertParagraph();
 builder.insertField(" MERGEFIELD Company ");
 builder.insertParagraph();
 builder.insertField(" MERGEFIELD Address ");
 builder.insertParagraph();
 builder.insertField(" MERGEFIELD City ");

 doc.getMailMerge().execute(new String[]{"FullName", "Company", "Address", "City"},
         new Object[]{"James Bond", "MI5 Headquarters", "Milbank", "London"});
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [ATTACHMENT](#ATTACHMENT) | Invia il documento al browser e presenta un'opzione per salvare il documento su disco o aprirlo nell'applicazione associata all'estensione del documento. |
| [INLINE](#INLINE) | Invia il documento al browser e presenta un'opzione per salvare il documento su disco o aprirlo all'interno del browser. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String contentDispositionName)](#fromName-java.lang.String) |  |
| [getName(int contentDisposition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int contentDisposition)](#toString-int) |  |
### ATTACHMENT {#ATTACHMENT}
```
public static int ATTACHMENT
```


Invia il documento al browser e presenta un'opzione per salvare il documento su disco o aprirlo nell'applicazione associata all'estensione del documento.

### INLINE {#INLINE}
```
public static int INLINE
```


Invia il documento al browser e presenta un'opzione per salvare il documento su disco o aprirlo all'interno del browser.

### length {#length}
```
public static int length
```


### fromName(String contentDispositionName) {#fromName-java.lang.String}
```
public static int fromName(String contentDispositionName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| contentDispositionName | java.lang.String |  |

**Returns:**
int
### getName(int contentDisposition) {#getName-int}
```
public static String getName(int contentDisposition)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| contentDisposition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int contentDisposition) {#toString-int}
```
public static String toString(int contentDisposition)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| contentDisposition | int |  |

**Returns:**
java.lang.String
