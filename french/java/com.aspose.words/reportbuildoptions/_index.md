---
title: "ReportBuildOptions"
linktitle: "ReportBuildOptions"
second_title: "Aspose.Words pour Java"
description: "Spécifie les options contrôlant le comportement de ReportingEngine lors de la génération d'un rapport en Java."
type: docs
weight: 570
url: /fr/java/com.aspose.words/reportbuildoptions/
---

**Inheritance:**
java.lang.Object
```
public class ReportBuildOptions
```

Spécifie les options contrôlant le comportement de [ReportingEngine](../../com.aspose.words/reportingengine/) lors de la génération d'un rapport.
## Champs

| Champ | Description |
| --- | --- |
| [ALLOW_MISSING_MEMBERS](#ALLOW-MISSING-MEMBERS) | Spécifie que les membres d'objet manquants doivent être traités comme des littéraux null par le moteur. |
| [INLINE_ERROR_MESSAGES](#INLINE-ERROR-MESSAGES) | Spécifie que le moteur doit intégrer les messages d'erreur de syntaxe de modèle directement dans les documents de sortie. |
| [NONE](#NONE) | Spécifie les options par défaut. |
| [REMOVE_EMPTY_PARAGRAPHS](#REMOVE-EMPTY-PARAGRAPHS) | Spécifie que le moteur doit supprimer les paragraphes devenus vides après la suppression ou le remplacement par des valeurs vides des balises de syntaxe de modèle. |
| [RESPECT_JPEG_EXIF_ORIENTATION](#RESPECT-JPEG-EXIF-ORIENTATION) | Spécifie que le moteur doit utiliser les valeurs d'orientation d'image EXIF \\\\u200b\\\\u200bimage pour faire pivoter correctement les images JPEG insérées. |
| [UPDATE_FIELDS_SYNTAX_AWARE](#UPDATE-FIELDS-SYNTAX-AWARE) | Spécifie que le moteur doit ignorer la syntaxe de modèle dans les résultats de champ et mettre à jour les champs après la génération d'un rapport. |
| [USE_LEGACY_HEADER_FOOTER_VISITING](#USE-LEGACY-HEADER-FOOTER-VISITING) | Spécifie que le moteur doit parcourir les nœuds enfants de section (en-têtes, pieds de page, corps) dans un ordre compatible avec les versions d'Aspose.Words antérieures à 21.9. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String reportBuildOptionsName)](#fromName-java.lang.String) |  |
| [fromNames(Set reportBuildOptionsNames)](#fromNames-java.util.Set) |  |
| [getName(int reportBuildOptions)](#getName-int) |  |
| [getNames(int reportBuildOptions)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int reportBuildOptions)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### ALLOW_MISSING_MEMBERS {#ALLOW-MISSING-MEMBERS}
```
public static int ALLOW_MISSING_MEMBERS
```


Spécifie que les membres d'objet manquants doivent être traités comme des littéraux null par le moteur. Cette option n'affecte que l'accès aux membres d'objet d'instance (c'est‑à‑dire non statiques) et aux méthodes d'extension. Si cette option n'est pas définie, le moteur lève une exception lorsqu'il rencontre un membre d'objet manquant.

### INLINE_ERROR_MESSAGES {#INLINE-ERROR-MESSAGES}
```
public static int INLINE_ERROR_MESSAGES
```


Spécifie que le moteur doit incorporer les messages d'erreur de syntaxe de modèle directement dans les documents de sortie. Si cette option n'est pas définie, le moteur lève une exception lorsqu'il rencontre une erreur de syntaxe.

### NONE {#NONE}
```
public static int NONE
```


Spécifie les options par défaut.

### REMOVE_EMPTY_PARAGRAPHS {#REMOVE-EMPTY-PARAGRAPHS}
```
public static int REMOVE_EMPTY_PARAGRAPHS
```


Spécifie que le moteur doit supprimer les paragraphes devenus vides après la suppression ou le remplacement par des valeurs vides des balises de syntaxe de modèle.

### RESPECT_JPEG_EXIF_ORIENTATION {#RESPECT-JPEG-EXIF-ORIENTATION}
```
public static int RESPECT_JPEG_EXIF_ORIENTATION
```


Spécifie que le moteur doit utiliser les valeurs d'orientation d'image EXIF \\\\u200b\\\\u200bimage pour faire pivoter correctement les images JPEG insérées.

### UPDATE_FIELDS_SYNTAX_AWARE {#UPDATE-FIELDS-SYNTAX-AWARE}
```
public static int UPDATE_FIELDS_SYNTAX_AWARE
```


Spécifie que le moteur doit ignorer la syntaxe de modèle dans les résultats de champ et mettre à jour les champs après la génération d'un rapport.

### USE_LEGACY_HEADER_FOOTER_VISITING {#USE-LEGACY-HEADER-FOOTER-VISITING}
```
public static int USE_LEGACY_HEADER_FOOTER_VISITING
```


Spécifie que le moteur doit parcourir les nœuds enfants de section (en-têtes, pieds de page, corps) dans un ordre compatible avec les versions d'Aspose.Words antérieures à 21.9.

 **Remarks:** 

Par défaut, le moteur traite les en-têtes et pieds de page comme s'ils étaient liés aux sauts de section. Ainsi, lors du parcours des nœuds enfants de section, le corps est parcouru en premier, puis les en-têtes et pieds de page. Cela correspond au comportement de Microsoft Word lors du copier‑coller ou de la suppression de contenus multi‑sections et produit des résultats plus corrects dans la plupart des scénarios.

Avant Aspose.Words 21.9, le moteur utilisait un autre ordre de visite : les nœuds enfants de section étaient parcourus dans l'ordre où ils apparaissent dans le document. Appliquez cette valeur à [ReportingEngine.getOptions()](../../com.aspose.words/reportingengine/\#getOptions) / [ReportingEngine.setOptions(int)](../../com.aspose.words/reportingengine/\#setOptions-int) si la compatibilité avec les versions antérieures d'Aspose.Words est requise.

### length {#length}
```
public static int length
```


### fromName(String reportBuildOptionsName) {#fromName-java.lang.String}
```
public static int fromName(String reportBuildOptionsName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| reportBuildOptionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set reportBuildOptionsNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set reportBuildOptionsNames)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| reportBuildOptionsNames | java.util.Set |  |

**Returns:**
int
### getName(int reportBuildOptions) {#getName-int}
```
public static String getName(int reportBuildOptions)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| reportBuildOptions | int |  |

**Returns:**
java.lang.String
### getNames(int reportBuildOptions) {#getNames-int}
```
public static Set getNames(int reportBuildOptions)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| reportBuildOptions | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int reportBuildOptions) {#toString-int}
```
public static String toString(int reportBuildOptions)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| reportBuildOptions | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
