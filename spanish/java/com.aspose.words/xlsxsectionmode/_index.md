---
title: "XlsxSectionMode"
linktitle: "XlsxSectionMode"
second_title: "Aspose.Words para Java"
description: "Especifica cómo se manejan las secciones al guardar un documento en formato XLSX en Java."
type: docs
weight: 744
url: /es/java/com.aspose.words/xlsxsectionmode/
---

**Inheritance:**
java.lang.Object
```
public class XlsxSectionMode
```

Especifica cómo se manejan las secciones al guardar un documento en formato XLSX.

 **Examples:** 

Muestra cómo guardar el documento como hojas de cálculo separadas.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 // Each section of a document will be created as a separate worksheet.
 // Use 'SingleWorksheet' to display all document on one worksheet.
 XlsxSaveOptions xlsxSaveOptions = new XlsxSaveOptions();
 xlsxSaveOptions.setSectionMode(XlsxSectionMode.MULTIPLE_WORKSHEETS);

 doc.save(getArtifactsDir() + "XlsxSaveOptions.SelectionMode.xlsx", xlsxSaveOptions);
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [MULTIPLE_WORKSHEETS](#MULTIPLE-WORKSHEETS) | Especifica que se crea una hoja de cálculo separada para cada sección de un documento. |
| [SINGLE_WORKSHEET](#SINGLE-WORKSHEET) | Especifica que todas las secciones de un documento se guardan en una sola hoja de cálculo. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String xlsxSectionModeName)](#fromName-java.lang.String) |  |
| [getName(int xlsxSectionMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int xlsxSectionMode)](#toString-int) |  |
### MULTIPLE_WORKSHEETS {#MULTIPLE-WORKSHEETS}
```
public static int MULTIPLE_WORKSHEETS
```


Especifica que se crea una hoja de cálculo separada para cada sección de un documento.

### SINGLE_WORKSHEET {#SINGLE-WORKSHEET}
```
public static int SINGLE_WORKSHEET
```


Especifica que todas las secciones de un documento se guardan en una sola hoja de cálculo.

### length {#length}
```
public static int length
```


### fromName(String xlsxSectionModeName) {#fromName-java.lang.String}
```
public static int fromName(String xlsxSectionModeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| xlsxSectionModeName | java.lang.String |  |

**Returns:**
int
### getName(int xlsxSectionMode) {#getName-int}
```
public static String getName(int xlsxSectionMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| xlsxSectionMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int xlsxSectionMode) {#toString-int}
```
public static String toString(int xlsxSectionMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| xlsxSectionMode | int |  |

**Returns:**
java.lang.String
