---
title: "TxtOfficeMathExportMode"
linktitle: "TxtOfficeMathExportMode"
second_title: "Aspose.Words para Java"
description: "Especifica cómo Aspose.Words exporta OfficeMath a SaveFormat.TEXT en Java."
type: docs
weight: 694
url: /es/java/com.aspose.words/txtofficemathexportmode/
---

**Inheritance:**
java.lang.Object
```
public class TxtOfficeMathExportMode
```

Especifica cómo Aspose.Words exporta OfficeMath a [SaveFormat.TEXT](../../com.aspose.words/saveformat/\#TEXT).

 **Examples:** 

Muestra cómo exportar el objeto OfficeMath como Latex en TXT.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 TxtSaveOptions saveOptions = new TxtSaveOptions();
 saveOptions.setOfficeMathExportMode(TxtOfficeMathExportMode.LATEX);

 doc.save(getArtifactsDir() + "TxtSaveOptions.ExportOfficeMathAsLatexToText.txt", saveOptions);
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [LATEX](#LATEX) | Exportar OfficeMath como LaTeX. |
| [TEXT](#TEXT) | Exportar OfficeMath como texto plano. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String txtOfficeMathExportModeName)](#fromName-java.lang.String) |  |
| [getName(int txtOfficeMathExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int txtOfficeMathExportMode)](#toString-int) |  |
### LATEX {#LATEX}
```
public static int LATEX
```


Exportar OfficeMath como LaTeX.

### TEXT {#TEXT}
```
public static int TEXT
```


Exportar OfficeMath como texto plano.

### length {#length}
```
public static int length
```


### fromName(String txtOfficeMathExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String txtOfficeMathExportModeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| txtOfficeMathExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int txtOfficeMathExportMode) {#getName-int}
```
public static String getName(int txtOfficeMathExportMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| txtOfficeMathExportMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int txtOfficeMathExportMode) {#toString-int}
```
public static String toString(int txtOfficeMathExportMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| txtOfficeMathExportMode | int |  |

**Returns:**
java.lang.String
