---
title: "PdfCompliance"
linktitle: "PdfCompliance"
second_title: "Aspose.Words für Java"
description: "Gibt das Konformitätsniveau der PDF‑Standards in Java an."
type: docs
weight: 529
url: /de/java/com.aspose.words/pdfcompliance/
---

**Inheritance:**
java.lang.Object
```
public class PdfCompliance
```

Gibt das Konformitätsniveau der PDF-Standards an.

 **Examples:** 

Zeigt, wie das Konformitätsniveau der PDF‑Standards für gespeicherte PDF‑Dokumente festgelegt wird.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [PDF_17](#PDF-17) | Die Ausgabedatei entspricht dem PDF 1.7‑Standard (ISO 32000‑1). |
| [PDF_20](#PDF-20) | Die Ausgabedatei entspricht dem PDF 2.0‑Standard (ISO 32000‑2). |
| [PDF_A_1_A](#PDF-A-1-A) | Die Ausgabedatei entspricht dem PDF/A‑1a‑Standard (ISO 19005‑1). |
| [PDF_A_1_B](#PDF-A-1-B) | Die Ausgabedatei entspricht dem PDF/A‑1b‑Standard (ISO 19005‑1). |
| [PDF_A_2_A](#PDF-A-2-A) | Die Ausgabedatei entspricht dem PDF/A‑2a‑Standard (ISO 19005‑2). |
| [PDF_A_2_U](#PDF-A-2-U) | Die Ausgabedatei entspricht dem PDF/A‑2u‑Standard (ISO 19005‑2). |
| [PDF_A_3_A](#PDF-A-3-A) | Die Ausgabedatei entspricht dem PDF/A‑3a‑Standard (ISO 19005‑3). |
| [PDF_A_3_U](#PDF-A-3-U) | Die Ausgabedatei entspricht dem PDF/A‑3u‑Standard (ISO 19005‑3). |
| [PDF_A_4](#PDF-A-4) | Die Ausgabedatei entspricht dem PDF/A‑4‑Standard (ISO 19005‑4:2020). |
| [PDF_A_4_F](#PDF-A-4-F) | Die Ausgabedatei entspricht dem PDF/A‑4f‑Standard (ISO 19005‑4:2020). |
| [PDF_A_4_UA_2](#PDF-A-4-UA-2) | Die Ausgabedatei entspricht sowohl dem PDF/A‑4‑Standard (ISO 19005‑4:2020) als auch dem PDF/UA‑2‑Standard (ISO 14289‑2:2024). |
| [PDF_UA_1](#PDF-UA-1) | Die Ausgabedatei entspricht dem PDF/UA‑1‑Standard (ISO 14289‑1). |
| [PDF_UA_2](#PDF-UA-2) | Die Ausgabedatei entspricht dem PDF/UA‑2‑Standard (ISO 14289‑2:2024). |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String pdfComplianceName)](#fromName-java.lang.String) |  |
| [getName(int pdfCompliance)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfCompliance)](#toString-int) |  |
### PDF_17 {#PDF-17}
```
public static int PDF_17
```


Die Ausgabedatei entspricht dem PDF 1.7‑Standard (ISO 32000‑1).

### PDF_20 {#PDF-20}
```
public static int PDF_20
```


Die Ausgabedatei entspricht dem PDF 2.0‑Standard (ISO 32000‑2).

### PDF_A_1_A {#PDF-A-1-A}
```
public static int PDF_A_1_A
```


Die Ausgabedatei entspricht dem PDF/A-1a (ISO 19005-1) Standard. Diese Stufe beinhaltet alle Anforderungen von PDF/A-1b und verlangt zusätzlich, dass die Dokumentenstruktur enthalten ist (auch als \"tagged\" bezeichnet), mit dem Ziel, sicherzustellen, dass Dokumentinhalte durchsucht und wiederverwendet werden können.

 **Remarks:** 

Beachten Sie, dass das Exportieren der Dokumentenstruktur den Speicherverbrauch erheblich erhöht, insbesondere bei großen Dokumenten.

### PDF_A_1_B {#PDF-A-1-B}
```
public static int PDF_A_1_B
```


Die Ausgabedatei entspricht dem PDF/A-1b (ISO 19005-1) Standard. PDF/A-1b hat das Ziel, eine zuverlässige Reproduktion des visuellen Erscheinungsbildes des Dokuments zu gewährleisten.

### PDF_A_2_A {#PDF-A-2-A}
```
public static int PDF_A_2_A
```


Die Ausgabedatei entspricht dem PDF/A-2a (ISO 19005-2) Standard. Diese Stufe beinhaltet alle Anforderungen von PDF/A-2u und verlangt zusätzlich, dass die Dokumentenstruktur enthalten ist (auch als \"tagged\" bezeichnet), mit dem Ziel, sicherzustellen, dass Dokumentinhalte durchsucht und wiederverwendet werden können.

 **Remarks:** 

Beachten Sie, dass das Exportieren der Dokumentenstruktur den Speicherverbrauch erheblich erhöht, insbesondere bei großen Dokumenten.

### PDF_A_2_U {#PDF-A-2-U}
```
public static int PDF_A_2_U
```


Die Ausgabedatei entspricht dem PDF/A-2u (ISO 19005-2) Standard. PDF/A-2u hat das Ziel, das statische visuelle Erscheinungsbild des Dokuments über die Zeit hinweg zu erhalten, unabhängig von den Werkzeugen und Systemen, die zum Erstellen, Speichern oder Rendern der Dateien verwendet werden. Zusätzlich kann jeder im Dokument enthaltene Text zuverlässig als Reihe von Unicode-Codepunkten extrahiert werden.

### PDF_A_3_A {#PDF-A-3-A}
```
public static int PDF_A_3_A
```


Die Ausgabedatei entspricht dem PDF/A-3a (ISO 19005-3) Standard. Diese Stufe beinhaltet alle Anforderungen von PDF/A-3u und verlangt zusätzlich, dass die Dokumentenstruktur enthalten ist (auch als \"tagged\" bezeichnet), mit dem Ziel, sicherzustellen, dass Dokumentinhalte durchsucht und wiederverwendet werden können.

 **Remarks:** 

Beachten Sie, dass das Exportieren der Dokumentenstruktur den Speicherverbrauch erheblich erhöht, insbesondere bei großen Dokumenten.

### PDF_A_3_U {#PDF-A-3-U}
```
public static int PDF_A_3_U
```


Die Ausgabedatei entspricht dem PDF/A-3u (ISO 19005-3) Standard. PDF/A-3u (wie auch PDF/A-2u) hat das Ziel, das statische visuelle Erscheinungsbild des Dokuments über die Zeit hinweg zu erhalten, unabhängig von den Werkzeugen und Systemen, die zum Erstellen, Speichern oder Rendern der Dateien verwendet werden. Zusätzlich kann jeder im Dokument enthaltene Text zuverlässig als Reihe von Unicode-Codepunkten extrahiert werden. Zusätzlich zu PDF/A-2u ermöglicht PDF/A-3u das Einbetten von Anhängen in das PDF-Dokument.

### PDF_A_4 {#PDF-A-4}
```
public static int PDF_A_4
```


Die Ausgabedatei entspricht dem PDF/A-4 (ISO 19005-4:2020) Standard. PDF/A-4 hat das Ziel, das statische visuelle Erscheinungsbild des Dokuments über die Zeit hinweg zu erhalten, unabhängig von den Werkzeugen und Systemen, die zum Erstellen, Speichern oder Rendern der Dateien verwendet werden. Zusätzlich kann jeder im Dokument enthaltene Text zuverlässig als Reihe von Unicode-Codepunkten extrahiert werden.

### PDF_A_4_F {#PDF-A-4-F}
```
public static int PDF_A_4_F
```


Die Ausgabedatei entspricht dem PDF/A-4f (ISO 19005-4:2020) Standard. Diese Stufe beinhaltet alle Anforderungen von PDF/A-4 und erlaubt zusätzlich das Einbetten von Anhängen in das PDF-Dokument.

### PDF_A_4_UA_2 {#PDF-A-4-UA-2}
```
public static int PDF_A_4_UA_2
```


Die Ausgabedatei entspricht sowohl dem PDF/A-4 (ISO 19005-4:2020) als auch dem PDF/UA-2 (ISO 14289-2:2024) Standard. PDF/A-4 hat das Ziel, das statische visuelle Erscheinungsbild des Dokuments über die Zeit hinweg zu erhalten, unabhängig von den Werkzeugen und Systemen, die zum Erstellen, Speichern oder Rendern der Dateien verwendet werden. Der Hauptzweck von PDF/UA besteht darin, zu definieren, wie elektronische Dokumente im PDF-Format dargestellt werden können, sodass die Datei zugänglich ist.

 **Remarks:** 

Beachten Sie, dass das Exportieren der Dokumentenstruktur den Speicherverbrauch erheblich erhöht, insbesondere bei großen Dokumenten.

### PDF_UA_1 {#PDF-UA-1}
```
public static int PDF_UA_1
```


Die Ausgabedatei entspricht dem PDF/UA-1 (ISO 14289-1) Standard. Der Hauptzweck von PDF/UA ist es, zu definieren, wie elektronische Dokumente im PDF-Format dargestellt werden, sodass die Datei zugänglich ist.

 **Remarks:** 

Beachten Sie, dass das Exportieren der Dokumentenstruktur den Speicherverbrauch erheblich erhöht, insbesondere bei großen Dokumenten.

### PDF_UA_2 {#PDF-UA-2}
```
public static int PDF_UA_2
```


Die Ausgabedatei entspricht dem PDF/UA-2 (ISO 14289-2:2024) Standard. Der Hauptzweck von PDF/UA ist es, zu definieren, wie elektronische Dokumente im PDF-Format dargestellt werden, sodass die Datei zugänglich ist.

 **Remarks:** 

Beachten Sie, dass das Exportieren der Dokumentenstruktur den Speicherverbrauch erheblich erhöht, insbesondere bei großen Dokumenten.

### length {#length}
```
public static int length
```


### fromName(String pdfComplianceName) {#fromName-java.lang.String}
```
public static int fromName(String pdfComplianceName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pdfComplianceName | java.lang.String |  |

**Returns:**
int
### getName(int pdfCompliance) {#getName-int}
```
public static String getName(int pdfCompliance)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pdfCompliance | int |  |

**Returns:**
java.lang.String
