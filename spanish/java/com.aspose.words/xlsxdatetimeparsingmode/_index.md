---
title: "XlsxDateTimeParsingMode"
linktitle: "XlsxDateTimeParsingMode"
second_title: "Aspose.Words para Java"
description: "Especifica cómo se analiza el texto del documento para identificar valores de fecha y hora en Java."
type: docs
weight: 742
url: /es/java/com.aspose.words/xlsxdatetimeparsingmode/
---

**Inheritance:**
java.lang.Object
```
public class XlsxDateTimeParsingMode
```

Especifica cómo se analiza el texto del documento para identificar valores de fecha y hora.

 **Examples:** 

Muestra cómo especificar la autodetección del formato de fecha y hora.

```

 Document doc = new Document(getMyDir() + "Xlsx DateTime.docx");

 XlsxSaveOptions saveOptions = new XlsxSaveOptions();
 // Specify using datetime format autodetection.
 saveOptions.setDateTimeParsingMode(XlsxDateTimeParsingMode.AUTO);

 doc.save(getArtifactsDir() + "XlsxSaveOptions.DateTimeParsingMode.xlsx", saveOptions);
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [AUTO](#AUTO) | El formato de fecha y hora usado en un documento se determina automáticamente. |
| [USE_CURRENT_LOCALE](#USE-CURRENT-LOCALE) | El formato de fecha y hora establecido para el hilo actual se usa primero para analizar valores de cadena. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String xlsxDateTimeParsingModeName)](#fromName-java.lang.String) |  |
| [getName(int xlsxDateTimeParsingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int xlsxDateTimeParsingMode)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


El formato de fecha y hora usado en un documento se determina automáticamente. Esto puede requerir tiempo adicional.

### USE_CURRENT_LOCALE {#USE-CURRENT-LOCALE}
```
public static int USE_CURRENT_LOCALE
```


El formato de fecha y hora establecido para el hilo actual se usa primero para analizar valores de cadena. Si el análisis falla, se prueban otros formatos de fecha y hora comunes.

### length {#length}
```
public static int length
```


### fromName(String xlsxDateTimeParsingModeName) {#fromName-java.lang.String}
```
public static int fromName(String xlsxDateTimeParsingModeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| xlsxDateTimeParsingModeName | java.lang.String |  |

**Returns:**
int
### getName(int xlsxDateTimeParsingMode) {#getName-int}
```
public static String getName(int xlsxDateTimeParsingMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| xlsxDateTimeParsingMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int xlsxDateTimeParsingMode) {#toString-int}
```
public static String toString(int xlsxDateTimeParsingMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| xlsxDateTimeParsingMode | int |  |

**Returns:**
java.lang.String
