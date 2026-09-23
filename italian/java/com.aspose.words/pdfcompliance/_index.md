---
title: "PdfCompliance"
linktitle: "PdfCompliance"
second_title: "Aspose.Words per Java"
description: "Specifica il livello di conformità agli standard PDF in Java."
type: docs
weight: 529
url: /it/java/com.aspose.words/pdfcompliance/
---

**Inheritance:**
java.lang.Object
```
public class PdfCompliance
```

Specifica il livello di conformità agli standard PDF.

 **Examples:** 

Mostra come impostare il livello di conformità agli standard PDF dei documenti PDF salvati.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 // Note that some PdfSaveOptions are prohibited when saving to one of the standards and automatically fixed.
 // Use IWarningCallback to know which options are automatically fixed.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Set the "Compliance" property to "PdfCompliance.PdfA1b" to comply with the "PDF/A-1b" standard,
 // which aims to preserve the visual appearance of the document as Aspose.Words convert it to PDF.
 // Set the "Compliance" property to "PdfCompliance.Pdf17" to comply with the "1.7" standard.
 // Set the "Compliance" property to "PdfCompliance.PdfA1a" to comply with the "PDF/A-1a" standard,
 // which complies with "PDF/A-1b" as well as preserving the document structure of the original document.
 // Set the "Compliance" property to "PdfCompliance.PdfUa1" to comply with the "PDF/UA-1" (ISO 14289-1) standard,
 // which aims to define represent electronic documents in PDF that allow the file to be accessible.
 // Set the "Compliance" property to "PdfCompliance.Pdf20" to comply with the "PDF 2.0" (ISO 32000-2) standard.
 // Set the "Compliance" property to "PdfCompliance.PdfA4" to comply with the "PDF/A-4" (ISO 19004:2020) standard,
 // which preserving document static visual appearance over time.
 // Set the "Compliance" property to "PdfCompliance.PdfA4Ua2" to comply with both PDF/A-4 (ISO 19005-4:2020)
 // and PDF/UA-2 (ISO 14289-2:2024) standards.
 // Set the "Compliance" property to "PdfCompliance.PdfUa2" to comply with the PDF/UA-2 (ISO 14289-2:2024) standard.
 // This helps with making documents searchable but may significantly increase the size of already large documents.
 saveOptions.setCompliance(pdfCompliance);

 doc.save(getArtifactsDir() + "PdfSaveOptions.Compliance.pdf", saveOptions);
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [PDF_17](#PDF-17) | Il file di output sarà conforme allo standard PDF 1.7 (ISO 32000-1). |
| [PDF_20](#PDF-20) | Il file di output sarà conforme allo standard PDF 2.0 (ISO 32000-2). |
| [PDF_A_1_A](#PDF-A-1-A) | Il file di output sarà conforme allo standard PDF/A-1a (ISO 19005-1). |
| [PDF_A_1_B](#PDF-A-1-B) | Il file di output sarà conforme allo standard PDF/A-1b (ISO 19005-1). |
| [PDF_A_2_A](#PDF-A-2-A) | Il file di output sarà conforme allo standard PDF/A-2a (ISO 19005-2). |
| [PDF_A_2_U](#PDF-A-2-U) | Il file di output sarà conforme allo standard PDF/A-2u (ISO 19005-2). |
| [PDF_A_3_A](#PDF-A-3-A) | Il file di output sarà conforme allo standard PDF/A-3a (ISO 19005-3). |
| [PDF_A_3_U](#PDF-A-3-U) | Il file di output sarà conforme allo standard PDF/A-3u (ISO 19005-3). |
| [PDF_A_4](#PDF-A-4) | Il file di output sarà conforme allo standard PDF/A-4 (ISO 19005-4:2020). |
| [PDF_A_4_F](#PDF-A-4-F) | Il file di output sarà conforme allo standard PDF/A-4f (ISO 19005-4:2020). |
| [PDF_A_4_UA_2](#PDF-A-4-UA-2) | Il file di output sarà conforme sia allo standard PDF/A-4 (ISO 19005-4:2020) sia allo standard PDF/UA-2 (ISO 14289-2:2024). |
| [PDF_UA_1](#PDF-UA-1) | Il file di output sarà conforme allo standard PDF/UA-1 (ISO 14289-1). |
| [PDF_UA_2](#PDF-UA-2) | Il file di output sarà conforme allo standard PDF/UA-2 (ISO 14289-2:2024). |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String pdfComplianceName)](#fromName-java.lang.String) |  |
| [getName(int pdfCompliance)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfCompliance)](#toString-int) |  |
### PDF_17 {#PDF-17}
```
public static int PDF_17
```


Il file di output sarà conforme allo standard PDF 1.7 (ISO 32000-1).

### PDF_20 {#PDF-20}
```
public static int PDF_20
```


Il file di output sarà conforme allo standard PDF 2.0 (ISO 32000-2).

### PDF_A_1_A {#PDF-A-1-A}
```
public static int PDF_A_1_A
```


Il file di output sarà conforme allo standard PDF/A-1a (ISO 19005-1). Questo livello include tutti i requisiti di PDF/A-1b e richiede inoltre che sia inclusa la struttura del documento (nota anche come "taggata"), con l'obiettivo di garantire che il contenuto del documento possa essere ricercato e riutilizzato.

 **Remarks:** 

Nota che l'esportazione della struttura del documento aumenta significativamente il consumo di memoria, soprattutto per i documenti di grandi dimensioni.

### PDF_A_1_B {#PDF-A-1-B}
```
public static int PDF_A_1_B
```


Il file di output sarà conforme allo standard PDF/A-1b (ISO 19005-1). PDF/A-1b ha l'obiettivo di garantire una riproduzione affidabile dell'aspetto visivo del documento.

### PDF_A_2_A {#PDF-A-2-A}
```
public static int PDF_A_2_A
```


Il file di output sarà conforme allo standard PDF/A-2a (ISO 19005-2). Questo livello include tutti i requisiti di PDF/A-2u e richiede inoltre che sia inclusa la struttura del documento (nota anche come "taggata"), con l'obiettivo di garantire che il contenuto del documento possa essere ricercato e riutilizzato.

 **Remarks:** 

Nota che l'esportazione della struttura del documento aumenta significativamente il consumo di memoria, soprattutto per i documenti di grandi dimensioni.

### PDF_A_2_U {#PDF-A-2-U}
```
public static int PDF_A_2_U
```


Il file di output sarà conforme allo standard PDF/A-2u (ISO 19005-2). PDF/A-2u ha l'obiettivo di preservare l'aspetto visivo statico del documento nel tempo, indipendentemente dagli strumenti e dai sistemi utilizzati per creare, archiviare o visualizzare i file. Inoltre, qualsiasi testo contenuto nel documento può essere estratto in modo affidabile come una serie di punti di codice Unicode.

### PDF_A_3_A {#PDF-A-3-A}
```
public static int PDF_A_3_A
```


Il file di output sarà conforme allo standard PDF/A-3a (ISO 19005-3). Questo livello include tutti i requisiti di PDF/A-3u e richiede inoltre che sia inclusa la struttura del documento (nota anche come "taggata"), con l'obiettivo di garantire che il contenuto del documento possa essere ricercato e riutilizzato.

 **Remarks:** 

Nota che l'esportazione della struttura del documento aumenta significativamente il consumo di memoria, soprattutto per i documenti di grandi dimensioni.

### PDF_A_3_U {#PDF-A-3-U}
```
public static int PDF_A_3_U
```


Il file di output sarà conforme allo standard PDF/A-3u (ISO 19005-3). PDF/A-3u (così come PDF/A-2u) ha l'obiettivo di preservare l'aspetto visivo statico del documento nel tempo, indipendentemente dagli strumenti e dai sistemi utilizzati per creare, archiviare o visualizzare i file. Inoltre, qualsiasi testo contenuto nel documento può essere estratto in modo affidabile come una serie di punti di codice Unicode. Oltre a PDF/A-2u, PDF/A-3u consente l'incorporamento di allegati nel documento PDF.

### PDF_A_4 {#PDF-A-4}
```
public static int PDF_A_4
```


Il file di output sarà conforme allo standard PDF/A-4 (ISO 19005-4:2020). PDF/A-4 ha l'obiettivo di preservare l'aspetto visivo statico del documento nel tempo, indipendentemente dagli strumenti e dai sistemi utilizzati per creare, archiviare o visualizzare i file. Inoltre, qualsiasi testo contenuto nel documento può essere estratto in modo affidabile come una serie di punti di codice Unicode.

### PDF_A_4_F {#PDF-A-4-F}
```
public static int PDF_A_4_F
```


Il file di output sarà conforme allo standard PDF/A-4f (ISO 19005-4:2020). Questo livello include tutti i requisiti di PDF/A-4 e consente inoltre l'incorporamento di allegati nel documento PDF.

### PDF_A_4_UA_2 {#PDF-A-4-UA-2}
```
public static int PDF_A_4_UA_2
```


Il file di output sarà conforme sia allo standard PDF/A-4 (ISO 19005-4:2020) sia allo standard PDF/UA-2 (ISO 14289-2:2024). PDF/A-4 ha l'obiettivo di preservare l'aspetto visivo statico del documento nel tempo, indipendentemente dagli strumenti e dai sistemi utilizzati per creare, archiviare o visualizzare i file. Lo scopo principale di PDF/UA è definire come rappresentare i documenti elettronici nel formato PDF in modo da rendere il file accessibile.

 **Remarks:** 

Nota che l'esportazione della struttura del documento aumenta significativamente il consumo di memoria, soprattutto per i documenti di grandi dimensioni.

### PDF_UA_1 {#PDF-UA-1}
```
public static int PDF_UA_1
```


Il file di output sarà conforme allo standard PDF/UA-1 (ISO 14289-1). Lo scopo principale di PDF/UA è definire come rappresentare i documenti elettronici nel formato PDF in modo da rendere il file accessibile.

 **Remarks:** 

Nota che l'esportazione della struttura del documento aumenta significativamente il consumo di memoria, soprattutto per i documenti di grandi dimensioni.

### PDF_UA_2 {#PDF-UA-2}
```
public static int PDF_UA_2
```


Il file di output sarà conforme allo standard PDF/UA-2 (ISO 14289-2:2024). Lo scopo principale di PDF/UA è definire come rappresentare i documenti elettronici nel formato PDF in modo da rendere il file accessibile.

 **Remarks:** 

Nota che l'esportazione della struttura del documento aumenta significativamente il consumo di memoria, soprattutto per i documenti di grandi dimensioni.

### length {#length}
```
public static int length
```


### fromName(String pdfComplianceName) {#fromName-java.lang.String}
```
public static int fromName(String pdfComplianceName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pdfComplianceName | java.lang.String |  |

**Returns:**
int
### getName(int pdfCompliance) {#getName-int}
```
public static String getName(int pdfCompliance)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pdfCompliance | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pdfCompliance) {#toString-int}
```
public static String toString(int pdfCompliance)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pdfCompliance | int |  |

**Returns:**
java.lang.String
