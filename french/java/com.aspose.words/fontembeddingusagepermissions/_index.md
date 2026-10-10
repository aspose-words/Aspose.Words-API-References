---
title: "FontEmbeddingUsagePermissions"
linktitle: "FontEmbeddingUsagePermissions"
second_title: "Aspose.Words pour Java"
description: "Représente les autorisations d'utilisation de l'incorporation de polices en Java."
type: docs
weight: 322
url: /fr/java/com.aspose.words/fontembeddingusagepermissions/
---

**Inheritance:**
java.lang.Object
```
public class FontEmbeddingUsagePermissions
```

Représente les autorisations d'utilisation d'intégration de police.

 **Examples:** 

Montre comment obtenir les informations de droits de licence pour les polices incorporées (FontInfo).

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
## Champs

| Champ | Description |
| --- | --- |
| [EDITABLE](#EDITABLE) | La police peut être incorporée et peut être chargée temporairement sur d'autres systèmes. |
| [INSTALLABLE](#INSTALLABLE) | La police peut être incorporée et peut être installée de façon permanente pour être utilisée sur des systèmes distants, ou par d'autres utilisateurs. |
| [PRINT_AND_PREVIEW](#PRINT-AND-PREVIEW) | La police peut être incorporée et peut être chargée temporairement sur d'autres systèmes aux fins de visualisation ou d'impression du document. |
| [RESTRICTED_LICENSE](#RESTRICTED-LICENSE) | La police ne doit pas être modifiée, incorporée ou échangée de quelque manière que ce soit sans obtenir d'abord l'autorisation explicite du propriétaire légal. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String fontEmbeddingUsagePermissionsName)](#fromName-java.lang.String) |  |
| [getName(int fontEmbeddingUsagePermissions)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontEmbeddingUsagePermissions)](#toString-int) |  |
### EDITABLE {#EDITABLE}
```
public static int EDITABLE
```


La police peut être incorporée et peut être chargée temporairement sur d'autres systèmes.

 **Remarks:** 

Comme pour l'incorporation en aperçu et impression, les documents contenant des polices modifiables peuvent être ouverts en lecture. De plus, l'édition est autorisée, y compris la possibilité de formater du nouveau texte en utilisant la police incorporée, et les modifications peuvent être enregistrées.

### INSTALLABLE {#INSTALLABLE}
```
public static int INSTALLABLE
```


La police peut être incorporée et peut être installée de façon permanente pour être utilisée sur des systèmes distants, ou par d'autres utilisateurs.

### PRINT_AND_PREVIEW {#PRINT-AND-PREVIEW}
```
public static int PRINT_AND_PREVIEW
```


La police peut être incorporée et peut être chargée temporairement sur d'autres systèmes aux fins de visualisation ou d'impression du document.

 **Remarks:** 

Les documents contenant des polices d'aperçu et d'impression doivent être ouverts \u201clecture seule\u201d; aucune modification ne peut être appliquée au document.

### RESTRICTED_LICENSE {#RESTRICTED-LICENSE}
```
public static int RESTRICTED_LICENSE
```


La police ne doit pas être modifiée, incorporée ou échangée de quelque manière que ce soit sans obtenir d'abord l'autorisation explicite du propriétaire légal.

### length {#length}
```
public static int length
```


### fromName(String fontEmbeddingUsagePermissionsName) {#fromName-java.lang.String}
```
public static int fromName(String fontEmbeddingUsagePermissionsName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| fontEmbeddingUsagePermissionsName | java.lang.String |  |

**Returns:**
int
### getName(int fontEmbeddingUsagePermissions) {#getName-int}
```
public static String getName(int fontEmbeddingUsagePermissions)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| fontEmbeddingUsagePermissions | int |  |

**Returns:**
java.lang.String
