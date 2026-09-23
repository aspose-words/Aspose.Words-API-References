---
title: "XlsxDateTimeParsingMode"
linktitle: "XlsxDateTimeParsingMode"
second_title: "Aspose.Words pour Java"
description: "Spécifie comment le texte du document est analysé pour identifier les valeurs de date et d'heure en Java."
type: docs
weight: 742
url: /fr/java/com.aspose.words/xlsxdatetimeparsingmode/
---

**Inheritance:**
java.lang.Object
```
public class XlsxDateTimeParsingMode
```

Spécifie comment le texte du document est analysé pour identifier les valeurs de date et d'heure.

 **Examples:** 

Montre comment spécifier la détection automatique du format de date et d'heure.

```

 Document doc = new Document(getMyDir() + "Xlsx DateTime.docx");

 XlsxSaveOptions saveOptions = new XlsxSaveOptions();
 // Specify using datetime format autodetection.
 saveOptions.setDateTimeParsingMode(XlsxDateTimeParsingMode.AUTO);

 doc.save(getArtifactsDir() + "XlsxSaveOptions.DateTimeParsingMode.xlsx", saveOptions);
 
```
## Champs

| Champ | Description |
| --- | --- |
| [AUTO](#AUTO) | Le format de date et d'heure utilisé dans un document est déterminé automatiquement. |
| [USE_CURRENT_LOCALE](#USE-CURRENT-LOCALE) | Le format de date et d'heure défini pour le thread actuel est utilisé en premier pour analyser les valeurs de chaîne. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String xlsxDateTimeParsingModeName)](#fromName-java.lang.String) |  |
| [getName(int xlsxDateTimeParsingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int xlsxDateTimeParsingMode)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Le format de date et d'heure utilisé dans un document est déterminé automatiquement. Cela peut prendre du temps supplémentaire.

### USE_CURRENT_LOCALE {#USE-CURRENT-LOCALE}
```
public static int USE_CURRENT_LOCALE
```


Le format de date et d'heure défini pour le thread actuel est utilisé en premier pour analyser les valeurs de chaîne. Si l'analyse échoue, d'autres formats de date et d'heure courants sont essayés.

### length {#length}
```
public static int length
```


### fromName(String xlsxDateTimeParsingModeName) {#fromName-java.lang.String}
```
public static int fromName(String xlsxDateTimeParsingModeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| xlsxDateTimeParsingModeName | java.lang.String |  |

**Returns:**
int
### getName(int xlsxDateTimeParsingMode) {#getName-int}
```
public static String getName(int xlsxDateTimeParsingMode)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| xlsxDateTimeParsingMode | int |  |

**Returns:**
java.lang.String
