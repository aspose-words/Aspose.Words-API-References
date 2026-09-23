---
title: "OdsoDataSourceType"
linktitle: "OdsoDataSourceType"
second_title: "Aspose.Words pour Java"
description: "Spécifie le type de source de données externe à connecter dans le cadre des informations de connexion ODSO en Java."
type: docs
weight: 488
url: /fr/java/com.aspose.words/odsodatasourcetype/
---

**Inheritance:**
java.lang.Object
```
public class OdsoDataSourceType
```

Spécifie le type de la source de données externe à connecter dans le cadre des informations de connexion ODSO.

 **Remarks:** 

La spécification OOXML est très vague pour cette énumération. Je suppose qu'elle pourrait correspondre à l'énumération WdMergeSubType http://msdn.microsoft.com/en-us/library/bb237801.aspx.
## Champs

| Champ | Description |
| --- | --- |
| [ADDRESS_BOOK](#ADDRESS-BOOK) | Spécifie qu'un document donné a été connecté à un carnet d'adresses de contacts. |
| [DATABASE](#DATABASE) | Spécifie qu'un document donné a été connecté à une base de données. |
| [DEFAULT](#DEFAULT) | Égal à [NONE](../../com.aspose.words/odsodatasourcetype/\#NONE). |
| [DOCUMENT_1](#DOCUMENT-1) | Spécifie qu'un document donné a été connecté à un autre format de document pris en charge par l'application productrice. |
| [DOCUMENT_2](#DOCUMENT-2) | Spécifie qu'un document donné a été connecté à un autre format de document pris en charge par l'application productrice. |
| [EMAIL](#EMAIL) | Spécifie qu'un document donné a été connecté à une application de messagerie. |
| [LEGACY](#LEGACY) | Spécifie qu'un document donné a été connecté à un format de document hérité pris en charge par l'application productrice. Possiblement wdMergeSubTypeWord2000. |
| [MASTER](#MASTER) | Spécifie qu'un document donné a été connecté à une source de données qui agrège d'autres sources de données. |
| [NATIVE](#NATIVE) | Spécifie qu'un document donné a été connecté à un autre format de document natif à l'application productrice. |
| [NONE](#NONE) | Le type de la source de données externe n'est pas spécifié. |
| [TEXT](#TEXT) | Spécifie qu'un document donné a été connecté à un fichier texte. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String odsoDataSourceTypeName)](#fromName-java.lang.String) |  |
| [getName(int odsoDataSourceType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int odsoDataSourceType)](#toString-int) |  |
### ADDRESS_BOOK {#ADDRESS-BOOK}
```
public static int ADDRESS_BOOK
```


Spécifie qu'un document donné a été connecté à un carnet d'adresses de contacts. Possiblement wdMergeSubTypeOAL.

### DATABASE {#DATABASE}
```
public static int DATABASE
```


Spécifie qu'un document donné a été connecté à une base de données. Possiblement wdMergeSubTypeAccess.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Égal à [NONE](../../com.aspose.words/odsodatasourcetype/\#NONE).

### DOCUMENT_1 {#DOCUMENT-1}
```
public static int DOCUMENT_1
```


Spécifie qu'un document donné a été connecté à un autre format de document pris en charge par l'application productrice. Possiblement wdMergeSubTypeOLEDBWord.

### DOCUMENT_2 {#DOCUMENT-2}
```
public static int DOCUMENT_2
```


Spécifie qu'un document donné a été connecté à un autre format de document pris en charge par l'application productrice. Possiblement wdMergeSubTypeWorks.

### EMAIL {#EMAIL}
```
public static int EMAIL
```


Spécifie qu'un document donné a été connecté à une application de messagerie. Possiblement wdMergeSubTypeOutlook.

### LEGACY {#LEGACY}
```
public static int LEGACY
```


Spécifie qu'un document donné a été connecté à un format de document hérité pris en charge par l'application productrice. Possiblement wdMergeSubTypeWord2000.

### MASTER {#MASTER}
```
public static int MASTER
```


Spécifie qu'un document donné a été connecté à une source de données qui agrège d'autres sources de données.

### NATIVE {#NATIVE}
```
public static int NATIVE
```


Spécifie qu'un document donné a été connecté à un autre format de document natif à l'application productrice. Possiblement wdMergeSubTypeOLEDBText

### NONE {#NONE}
```
public static int NONE
```


Le type de la source de données externe n'est pas spécifié. Possiblement wdMergeSubTypeWord.

### TEXT {#TEXT}
```
public static int TEXT
```


Spécifie qu'un document donné a été connecté à un fichier texte. Possiblement wdMergeSubTypeOther.

### length {#length}
```
public static int length
```


### fromName(String odsoDataSourceTypeName) {#fromName-java.lang.String}
```
public static int fromName(String odsoDataSourceTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| odsoDataSourceTypeName | java.lang.String |  |

**Returns:**
int
### getName(int odsoDataSourceType) {#getName-int}
```
public static String getName(int odsoDataSourceType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| odsoDataSourceType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int odsoDataSourceType) {#toString-int}
```
public static String toString(int odsoDataSourceType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| odsoDataSourceType | int |  |

**Returns:**
java.lang.String
