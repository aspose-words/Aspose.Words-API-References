---
title: "DocumentRecoveryMode"
linktitle: "DocumentRecoveryMode"
second_title: "Aspose.Words pour Java"
description: "Spécifie les options de récupération disponibles lorsqu'un document rencontre des erreurs lors du chargement en Java."
type: docs
weight: 171
url: /fr/java/com.aspose.words/documentrecoverymode/
---

**Inheritance:**
java.lang.Object
```
public class DocumentRecoveryMode
```

Spécifie les options de récupération disponibles lorsqu'un document rencontre des erreurs lors du chargement.

 **Examples:** 

Montre comment tenter de récupérer un document si des erreurs sont survenues pendant le chargement.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setRecoveryMode(DocumentRecoveryMode.TRY_RECOVER);

 Document doc = new Document(getMyDir() + "Corrupted footnotes.docx", loadOptions);
 
```
## Champs

| Champ | Description |
| --- | --- |
| [NONE](#NONE) | Aucune récupération n'est tentée. |
| [TRY_RECOVER](#TRY-RECOVER) | Tente de récupérer le document tout en préservant le maximum de données possible. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String documentRecoveryModeName)](#fromName-java.lang.String) |  |
| [getName(int documentRecoveryMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int documentRecoveryMode)](#toString-int) |  |
### NONE {#NONE}
```
public static int NONE
```


Aucune récupération n'est tentée. Si le document est invalide, le chargement échouera avec une erreur.

### TRY_RECOVER {#TRY-RECOVER}
```
public static int TRY_RECOVER
```


Tente de récupérer le document tout en préservant le maximum de données possible.

### length {#length}
```
public static int length
```


### fromName(String documentRecoveryModeName) {#fromName-java.lang.String}
```
public static int fromName(String documentRecoveryModeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| documentRecoveryModeName | java.lang.String |  |

**Returns:**
int
### getName(int documentRecoveryMode) {#getName-int}
```
public static String getName(int documentRecoveryMode)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| documentRecoveryMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int documentRecoveryMode) {#toString-int}
```
public static String toString(int documentRecoveryMode)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| documentRecoveryMode | int |  |

**Returns:**
java.lang.String
