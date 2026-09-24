---
title: "PdfCompliance"
linktitle: "PdfCompliance"
second_title: "Aspose.Words para Java"
description: "Especifica el nivel de cumplimiento de los estándares PDF en Java."
type: docs
weight: 529
url: /es/java/com.aspose.words/pdfcompliance/
---

**Inheritance:**
java.lang.Object
```
public class PdfCompliance
```

Especifica el nivel de cumplimiento de los estándares PDF.

 **Examples:** 

Muestra cómo establecer el nivel de cumplimiento de los estándares PDF de los documentos PDF guardados.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [PDF_17](#PDF-17) | El archivo de salida cumplirá con el estándar PDF 1.7 (ISO 32000-1). |
| [PDF_20](#PDF-20) | El archivo de salida cumplirá con el estándar PDF 2.0 (ISO 32000-2). |
| [PDF_A_1_A](#PDF-A-1-A) | El archivo de salida cumplirá con la norma PDF/A-1a (ISO 19005-1). |
| [PDF_A_1_B](#PDF-A-1-B) | El archivo de salida cumplirá con la norma PDF/A-1b (ISO 19005-1). |
| [PDF_A_2_A](#PDF-A-2-A) | El archivo de salida cumplirá con la norma PDF/A-2a (ISO 19005-2). |
| [PDF_A_2_U](#PDF-A-2-U) | El archivo de salida cumplirá con la norma PDF/A-2u (ISO 19005-2). |
| [PDF_A_3_A](#PDF-A-3-A) | El archivo de salida cumplirá con la norma PDF/A-3a (ISO 19005-3). |
| [PDF_A_3_U](#PDF-A-3-U) | El archivo de salida cumplirá con la norma PDF/A-3u (ISO 19005-3). |
| [PDF_A_4](#PDF-A-4) | El archivo de salida cumplirá con la norma PDF/A-4 (ISO 19005-4:2020). |
| [PDF_A_4_F](#PDF-A-4-F) | El archivo de salida cumplirá con la norma PDF/A-4f (ISO 19005-4:2020). |
| [PDF_A_4_UA_2](#PDF-A-4-UA-2) | El archivo de salida cumplirá con ambas normas PDF/A-4 (ISO 19005-4:2020) y PDF/UA-2 (ISO 14289-2:2024). |
| [PDF_UA_1](#PDF-UA-1) | El archivo de salida cumplirá con la norma PDF/UA-1 (ISO 14289-1). |
| [PDF_UA_2](#PDF-UA-2) | El archivo de salida cumplirá con la norma PDF/UA-2 (ISO 14289-2:2024). |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String pdfComplianceName)](#fromName-java.lang.String) |  |
| [getName(int pdfCompliance)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfCompliance)](#toString-int) |  |
### PDF_17 {#PDF-17}
```
public static int PDF_17
```


El archivo de salida cumplirá con el estándar PDF 1.7 (ISO 32000-1).

### PDF_20 {#PDF-20}
```
public static int PDF_20
```


El archivo de salida cumplirá con el estándar PDF 2.0 (ISO 32000-2).

### PDF_A_1_A {#PDF-A-1-A}
```
public static int PDF_A_1_A
```


El archivo de salida cumplirá con la norma PDF/A-1a (ISO 19005-1). Este nivel incluye todos los requisitos de PDF/A-1b y, adicionalmente, requiere que se incluya la estructura del documento (también conocida como "etiquetado"), con el objetivo de garantizar que el contenido del documento pueda ser buscado y reutilizado.

 **Remarks:** 

Tenga en cuenta que exportar la estructura del documento incrementa significativamente el consumo de memoria, especialmente en documentos grandes.

### PDF_A_1_B {#PDF-A-1-B}
```
public static int PDF_A_1_B
```


El archivo de salida cumplirá con la norma PDF/A-1b (ISO 19005-1). PDF/A-1b tiene el objetivo de garantizar una reproducción fiable de la apariencia visual del documento.

### PDF_A_2_A {#PDF-A-2-A}
```
public static int PDF_A_2_A
```


El archivo de salida cumplirá con la norma PDF/A-2a (ISO 19005-2). Este nivel incluye todos los requisitos de PDF/A-2u y, adicionalmente, requiere que se incluya la estructura del documento (también conocida como "etiquetado"), con el objetivo de garantizar que el contenido del documento pueda ser buscado y reutilizado.

 **Remarks:** 

Tenga en cuenta que exportar la estructura del documento incrementa significativamente el consumo de memoria, especialmente en documentos grandes.

### PDF_A_2_U {#PDF-A-2-U}
```
public static int PDF_A_2_U
```


El archivo de salida cumplirá con la norma PDF/A-2u (ISO 19005-2). PDF/A-2u tiene el objetivo de preservar la apariencia visual estática del documento a lo largo del tiempo, independientemente de las herramientas y sistemas utilizados para crear, almacenar o renderizar los archivos. Además, cualquier texto contenido en el documento puede extraerse de manera fiable como una serie de puntos de código Unicode.

### PDF_A_3_A {#PDF-A-3-A}
```
public static int PDF_A_3_A
```


El archivo de salida cumplirá con la norma PDF/A-3a (ISO 19005-3). Este nivel incluye todos los requisitos de PDF/A-3u y, adicionalmente, requiere que se incluya la estructura del documento (también conocida como "etiquetado"), con el objetivo de garantizar que el contenido del documento pueda ser buscado y reutilizado.

 **Remarks:** 

Tenga en cuenta que exportar la estructura del documento incrementa significativamente el consumo de memoria, especialmente en documentos grandes.

### PDF_A_3_U {#PDF-A-3-U}
```
public static int PDF_A_3_U
```


El archivo de salida cumplirá con la norma PDF/A-3u (ISO 19005-3). PDF/A-3u (al igual que PDF/A-2u) tiene el objetivo de preservar la apariencia visual estática del documento a lo largo del tiempo, independientemente de las herramientas y sistemas utilizados para crear, almacenar o renderizar los archivos. Además, cualquier texto contenido en el documento puede extraerse de manera fiable como una serie de puntos de código Unicode. Además de PDF/A-2u, PDF/A-3u permite incrustar archivos adjuntos en el documento PDF.

### PDF_A_4 {#PDF-A-4}
```
public static int PDF_A_4
```


El archivo de salida cumplirá con la norma PDF/A-4 (ISO 19005-4:2020). PDF/A-4 tiene el objetivo de preservar la apariencia visual estática del documento a lo largo del tiempo, independientemente de las herramientas y sistemas utilizados para crear, almacenar o renderizar los archivos. Además, cualquier texto contenido en el documento puede extraerse de manera fiable como una serie de puntos de código Unicode.

### PDF_A_4_F {#PDF-A-4-F}
```
public static int PDF_A_4_F
```


El archivo de salida cumplirá con la norma PDF/A-4f (ISO 19005-4:2020). Este nivel incluye todos los requisitos de PDF/A-4 y, adicionalmente, permite incrustar archivos adjuntos en el documento PDF.

### PDF_A_4_UA_2 {#PDF-A-4-UA-2}
```
public static int PDF_A_4_UA_2
```


El archivo de salida cumplirá con ambas normas PDF/A-4 (ISO 19005-4:2020) y PDF/UA-2 (ISO 14289-2:2024). PDF/A-4 tiene el objetivo de preservar la apariencia visual estática del documento a lo largo del tiempo, independientemente de las herramientas y sistemas utilizados para crear, almacenar o renderizar los archivos. El propósito principal de PDF/UA es definir cómo representar documentos electrónicos en el formato PDF de manera que el archivo sea accesible.

 **Remarks:** 

Tenga en cuenta que exportar la estructura del documento incrementa significativamente el consumo de memoria, especialmente en documentos grandes.

### PDF_UA_1 {#PDF-UA-1}
```
public static int PDF_UA_1
```


El archivo de salida cumplirá con el estándar PDF/UA-1 (ISO 14289-1). El propósito principal de PDF/UA es definir cómo representar documentos electrónicos en el formato PDF de manera que el archivo sea accesible.

 **Remarks:** 

Tenga en cuenta que exportar la estructura del documento incrementa significativamente el consumo de memoria, especialmente en documentos grandes.

### PDF_UA_2 {#PDF-UA-2}
```
public static int PDF_UA_2
```


El archivo de salida cumplirá con el estándar PDF/UA-2 (ISO 14289-2:2024). El propósito principal de PDF/UA es definir cómo representar documentos electrónicos en el formato PDF de manera que el archivo sea accesible.

 **Remarks:** 

Tenga en cuenta que exportar la estructura del documento incrementa significativamente el consumo de memoria, especialmente en documentos grandes.

### length {#length}
```
public static int length
```


### fromName(String pdfComplianceName) {#fromName-java.lang.String}
```
public static int fromName(String pdfComplianceName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pdfComplianceName | java.lang.String |  |

**Returns:**
int
### getName(int pdfCompliance) {#getName-int}
```
public static String getName(int pdfCompliance)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pdfCompliance | int |  |

**Returns:**
java.lang.String
