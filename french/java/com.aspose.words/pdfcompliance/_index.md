---
title: "PdfCompliance"
linktitle: "PdfCompliance"
second_title: "Aspose.Words pour Java"
description: "Spécifie le niveau de conformité aux normes PDF en Java."
type: docs
weight: 529
url: /fr/java/com.aspose.words/pdfcompliance/
---

**Inheritance:**
java.lang.Object
```
public class PdfCompliance
```

Spécifie le niveau de conformité aux normes PDF.

 **Examples:** 

Montre comment définir le niveau de conformité aux normes PDF des documents PDF enregistrés.

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
## Champs

| Champ | Description |
| --- | --- |
| [PDF_17](#PDF-17) | Le fichier de sortie sera conforme à la norme PDF 1.7 (ISO 32000-1). |
| [PDF_20](#PDF-20) | Le fichier de sortie sera conforme à la norme PDF 2.0 (ISO 32000-2). |
| [PDF_A_1_A](#PDF-A-1-A) | Le fichier de sortie sera conforme à la norme PDF/A-1a (ISO 19005-1). |
| [PDF_A_1_B](#PDF-A-1-B) | Le fichier de sortie sera conforme à la norme PDF/A-1b (ISO 19005-1). |
| [PDF_A_2_A](#PDF-A-2-A) | Le fichier de sortie sera conforme à la norme PDF/A-2a (ISO 19005-2). |
| [PDF_A_2_U](#PDF-A-2-U) | Le fichier de sortie sera conforme à la norme PDF/A-2u (ISO 19005-2). |
| [PDF_A_3_A](#PDF-A-3-A) | Le fichier de sortie sera conforme à la norme PDF/A-3a (ISO 19005-3). |
| [PDF_A_3_U](#PDF-A-3-U) | Le fichier de sortie sera conforme à la norme PDF/A-3u (ISO 19005-3). |
| [PDF_A_4](#PDF-A-4) | Le fichier de sortie sera conforme à la norme PDF/A-4 (ISO 19005-4:2020). |
| [PDF_A_4_F](#PDF-A-4-F) | Le fichier de sortie sera conforme à la norme PDF/A-4f (ISO 19005-4:2020). |
| [PDF_A_4_UA_2](#PDF-A-4-UA-2) | Le fichier de sortie sera conforme aux normes PDF/A-4 (ISO 19005-4:2020) et PDF/UA-2 (ISO 14289-2:2024). |
| [PDF_UA_1](#PDF-UA-1) | Le fichier de sortie sera conforme à la norme PDF/UA-1 (ISO 14289-1). |
| [PDF_UA_2](#PDF-UA-2) | Le fichier de sortie sera conforme à la norme PDF/UA-2 (ISO 14289-2:2024). |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String pdfComplianceName)](#fromName-java.lang.String) |  |
| [getName(int pdfCompliance)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfCompliance)](#toString-int) |  |
### PDF_17 {#PDF-17}
```
public static int PDF_17
```


Le fichier de sortie sera conforme à la norme PDF 1.7 (ISO 32000-1).

### PDF_20 {#PDF-20}
```
public static int PDF_20
```


Le fichier de sortie sera conforme à la norme PDF 2.0 (ISO 32000-2).

### PDF_A_1_A {#PDF-A-1-A}
```
public static int PDF_A_1_A
```


Le fichier de sortie sera conforme à la norme PDF/A-1a (ISO 19005-1). Ce niveau inclut toutes les exigences de PDF/A-1b et exige en outre que la structure du document soit incluse (également connue sous le nom de "étiquetée"), dans le but de garantir que le contenu du document puisse être recherché et réutilisé.

 **Remarks:** 

Notez que l'exportation de la structure du document augmente considérablement la consommation de mémoire, en particulier pour les documents volumineux.

### PDF_A_1_B {#PDF-A-1-B}
```
public static int PDF_A_1_B
```


Le fichier de sortie sera conforme à la norme PDF/A-1b (ISO 19005-1). PDF/A-1b a pour objectif d'assurer une reproduction fiable de l'apparence visuelle du document.

### PDF_A_2_A {#PDF-A-2-A}
```
public static int PDF_A_2_A
```


Le fichier de sortie sera conforme à la norme PDF/A-2a (ISO 19005-2). Ce niveau inclut toutes les exigences de PDF/A-2u et exige en outre que la structure du document soit incluse (également connue sous le nom de "étiquetée"), dans le but de garantir que le contenu du document puisse être recherché et réutilisé.

 **Remarks:** 

Notez que l'exportation de la structure du document augmente considérablement la consommation de mémoire, en particulier pour les documents volumineux.

### PDF_A_2_U {#PDF-A-2-U}
```
public static int PDF_A_2_U
```


Le fichier de sortie sera conforme à la norme PDF/A-2u (ISO 19005-2). PDF/A-2u a pour objectif de préserver l'apparence visuelle statique du document dans le temps, indépendamment des outils et systèmes utilisés pour créer, stocker ou rendre les fichiers. De plus, tout texte contenu dans le document peut être extrait de manière fiable sous forme d'une série de points de code Unicode.

### PDF_A_3_A {#PDF-A-3-A}
```
public static int PDF_A_3_A
```


Le fichier de sortie sera conforme à la norme PDF/A-3a (ISO 19005-3). Ce niveau inclut toutes les exigences de PDF/A-3u et exige en outre que la structure du document soit incluse (également connue sous le nom de "étiquetée"), dans le but de garantir que le contenu du document puisse être recherché et réutilisé.

 **Remarks:** 

Notez que l'exportation de la structure du document augmente considérablement la consommation de mémoire, en particulier pour les documents volumineux.

### PDF_A_3_U {#PDF-A-3-U}
```
public static int PDF_A_3_U
```


Le fichier de sortie sera conforme à la norme PDF/A-3u (ISO 19005-3). PDF/A-3u (tout comme PDF/A-2u) a pour objectif de préserver l'apparence visuelle statique du document dans le temps, indépendamment des outils et systèmes utilisés pour créer, stocker ou rendre les fichiers. De plus, tout texte contenu dans le document peut être extrait de manière fiable sous forme d'une série de points de code Unicode. En plus de PDF/A-2u, PDF/A-3u permet l'intégration de pièces jointes au document PDF.

### PDF_A_4 {#PDF-A-4}
```
public static int PDF_A_4
```


Le fichier de sortie sera conforme à la norme PDF/A-4 (ISO 19005-4:2020). PDF/A-4 a pour objectif de préserver l'apparence visuelle statique du document dans le temps, indépendamment des outils et systèmes utilisés pour créer, stocker ou rendre les fichiers. De plus, tout texte contenu dans le document peut être extrait de manière fiable sous forme d'une série de points de code Unicode.

### PDF_A_4_F {#PDF-A-4-F}
```
public static int PDF_A_4_F
```


Le fichier de sortie sera conforme à la norme PDF/A-4f (ISO 19005-4:2020). Ce niveau inclut toutes les exigences de PDF/A-4 et permet en outre l'intégration de pièces jointes au document PDF.

### PDF_A_4_UA_2 {#PDF-A-4-UA-2}
```
public static int PDF_A_4_UA_2
```


Le fichier de sortie sera conforme aux normes PDF/A-4 (ISO 19005-4:2020) et PDF/UA-2 (ISO 14289-2:2024). PDF/A-4 a pour objectif de préserver l'apparence visuelle statique du document dans le temps, indépendamment des outils et systèmes utilisés pour créer, stocker ou rendre les fichiers. Le but principal de PDF/UA est de définir comment représenter les documents électroniques au format PDF de manière à rendre le fichier accessible.

 **Remarks:** 

Notez que l'exportation de la structure du document augmente considérablement la consommation de mémoire, en particulier pour les documents volumineux.

### PDF_UA_1 {#PDF-UA-1}
```
public static int PDF_UA_1
```


Le fichier de sortie sera conforme à la norme PDF/UA-1 (ISO 14289-1). Le but principal de PDF/UA est de définir comment représenter les documents électroniques au format PDF de manière à ce que le fichier soit accessible.

 **Remarks:** 

Notez que l'exportation de la structure du document augmente considérablement la consommation de mémoire, en particulier pour les documents volumineux.

### PDF_UA_2 {#PDF-UA-2}
```
public static int PDF_UA_2
```


Le fichier de sortie sera conforme à la norme PDF/UA-2 (ISO 14289-2:2024). Le but principal de PDF/UA est de définir comment représenter les documents électroniques au format PDF de manière à ce que le fichier soit accessible.

 **Remarks:** 

Notez que l'exportation de la structure du document augmente considérablement la consommation de mémoire, en particulier pour les documents volumineux.

### length {#length}
```
public static int length
```


### fromName(String pdfComplianceName) {#fromName-java.lang.String}
```
public static int fromName(String pdfComplianceName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| pdfComplianceName | java.lang.String |  |

**Returns:**
int
### getName(int pdfCompliance) {#getName-int}
```
public static String getName(int pdfCompliance)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| pdfCompliance | int |  |

**Returns:**
java.lang.String
