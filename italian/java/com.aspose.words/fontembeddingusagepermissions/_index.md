---
title: "FontEmbeddingUsagePermissions"
linktitle: "FontEmbeddingUsagePermissions"
second_title: "Aspose.Words per Java"
description: "Rappresenta le autorizzazioni di utilizzo dell'incorporamento dei font in Java."
type: docs
weight: 322
url: /it/java/com.aspose.words/fontembeddingusagepermissions/
---

**Inheritance:**
java.lang.Object
```
public class FontEmbeddingUsagePermissions
```

Rappresenta le autorizzazioni di utilizzo dell'incorporamento del font.

 **Examples:** 

Mostra come ottenere le informazioni sui diritti di licenza per i caratteri incorporati (FontInfo).

```

 Document doc = new Document(getMyDir() + "Embedded font rights.docx");

 // Get the list of document fonts.
 FontInfoCollection fontInfos = doc.getFontInfos();
 for (FontInfo fontInfo : fontInfos)
 {
     if (fontInfo.getEmbeddingLicensingRights() != null)
     {
         System.out.println(fontInfo.getEmbeddingLicensingRights().getEmbeddingUsagePermissions());
         System.out.println(fontInfo.getEmbeddingLicensingRights().getBitmapEmbeddingOnly());
         System.out.println(fontInfo.getEmbeddingLicensingRights().getNoSubsetting());
     }
 }
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [EDITABLE](#EDITABLE) | Il font può essere incorporato e può essere caricato temporaneamente su altri sistemi. |
| [INSTALLABLE](#INSTALLABLE) | Il font può essere incorporato e può essere installato permanentemente per l'uso su sistemi remoti o per l'uso da parte di altri utenti. |
| [PRINT_AND_PREVIEW](#PRINT-AND-PREVIEW) | Il font può essere incorporato e può essere caricato temporaneamente su altri sistemi per scopi di visualizzazione o stampa del documento. |
| [RESTRICTED_LICENSE](#RESTRICTED-LICENSE) | Il font non deve essere modificato, incorporato o scambiato in alcun modo senza prima ottenere il permesso esplicito del proprietario legale. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String fontEmbeddingUsagePermissionsName)](#fromName-java.lang.String) |  |
| [getName(int fontEmbeddingUsagePermissions)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontEmbeddingUsagePermissions)](#toString-int) |  |
### EDITABLE {#EDITABLE}
```
public static int EDITABLE
```


Il font può essere incorporato e può essere caricato temporaneamente su altri sistemi.

 **Remarks:** 

Come per l'incorporamento di Anteprima e Stampa, i documenti contenenti font Modificabili possono essere aperti in lettura. Inoltre, la modifica è consentita, inclusa la possibilità di formattare nuovo testo usando il font incorporato, e le modifiche possono essere salvate.

### INSTALLABLE {#INSTALLABLE}
```
public static int INSTALLABLE
```


Il font può essere incorporato e può essere installato permanentemente per l'uso su sistemi remoti o per l'uso da parte di altri utenti.

### PRINT_AND_PREVIEW {#PRINT-AND-PREVIEW}
```
public static int PRINT_AND_PREVIEW
```


Il font può essere incorporato e può essere caricato temporaneamente su altri sistemi per scopi di visualizzazione o stampa del documento.

 **Remarks:** 

I documenti contenenti font di Anteprima e Stampa devono essere aperti \u201csolo lettura\u201d; non è possibile apportare modifiche al documento.

### RESTRICTED_LICENSE {#RESTRICTED-LICENSE}
```
public static int RESTRICTED_LICENSE
```


Il font non deve essere modificato, incorporato o scambiato in alcun modo senza prima ottenere il permesso esplicito del proprietario legale.

### length {#length}
```
public static int length
```


### fromName(String fontEmbeddingUsagePermissionsName) {#fromName-java.lang.String}
```
public static int fromName(String fontEmbeddingUsagePermissionsName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fontEmbeddingUsagePermissionsName | java.lang.String |  |

**Returns:**
int
### getName(int fontEmbeddingUsagePermissions) {#getName-int}
```
public static String getName(int fontEmbeddingUsagePermissions)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fontEmbeddingUsagePermissions | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int fontEmbeddingUsagePermissions) {#toString-int}
```
public static String toString(int fontEmbeddingUsagePermissions)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fontEmbeddingUsagePermissions | int |  |

**Returns:**
java.lang.String
