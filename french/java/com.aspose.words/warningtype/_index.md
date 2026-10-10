---
title: "WarningType"
linktitle: "WarningType"
second_title: "Aspose.Words pour Java"
description: "Spécifie le type d'avertissement émis par Aspose.Words lors du chargement ou de l'enregistrement du document en Java."
type: docs
weight: 720
url: /fr/java/com.aspose.words/warningtype/
---

**Inheritance:**
java.lang.Object
```
public class WarningType
```

Spécifie le type d'avertissement émis par Aspose.Words lors du chargement ou de l'enregistrement du document.

 **Examples:** 

Montre comment définir la propriété permettant de trouver la correspondance la plus proche pour une police manquante parmi les sources de polices disponibles.

```

 // Open a document that contains text formatted with a font that does not exist in any of our font sources.
 Document doc = new Document(getMyDir() + "Missing font.docx");

 // Assign a callback for handling font substitution warnings.
 WarningInfoCollection warningCollector = new WarningInfoCollection();
 doc.setWarningCallback(warningCollector);

 // Set a default font name and enable font substitution.
 FontSettings fontSettings = new FontSettings();
 fontSettings.getSubstitutionSettings().getDefaultFontSubstitution().setDefaultFontName("Arial");
 fontSettings.getSubstitutionSettings().getFontInfoSubstitution().setEnabled(true);

 // Original font metrics should be used after font substitution.
 doc.getLayoutOptions().setKeepOriginalFontMetrics(true);

 // We will get a font substitution warning if we save a document with a missing font.
 doc.setFontSettings(fontSettings);
 doc.save(getArtifactsDir() + "FontSettings.EnableFontSubstitution.pdf");

 for (WarningInfo info : warningCollector)
 {
     if (info.getWarningType() == WarningType.FONT_SUBSTITUTION)
         System.out.println(info.getDescription());
 }
 
```
## Champs

| Champ | Description |
| --- | --- |
| [DATA_LOSS](#DATA-LOSS) | Perte de données générique, aucun code spécifique. |
| [DATA_LOSS_CATEGORY](#DATA-LOSS-CATEGORY) | Du texte/caractère/image ou d'autres données seront manquants soit dans l'arbre du document après le chargement, soit dans le document créé après l'enregistrement. |
| [FONT_EMBEDDING](#FONT-EMBEDDING) | Perte d'informations de police incorporées lors de l'enregistrement du document. |
| [FONT_SUBSTITUTION](#FONT-SUBSTITUTION) | La police a été substituée. |
| [HINT](#HINT) | Avertit d'un problème potentiel ou suggère une amélioration. |
| [MAJOR_FORMATTING_LOSS](#MAJOR-FORMATTING-LOSS) | Perte de mise en forme majeure générique, aucun code spécifique. |
| [MAJOR_FORMATTING_LOSS_CATEGORY](#MAJOR-FORMATTING-LOSS-CATEGORY) | Le document résultant ou un emplacement particulier dans celui-ci peut sembler sensiblement différent par rapport au document original. |
| [MINOR_FORMATTING_LOSS](#MINOR-FORMATTING-LOSS) | Perte de mise en forme mineure générique, aucun code spécifique. |
| [MINOR_FORMATTING_LOSS_CATEGORY](#MINOR-FORMATTING-LOSS-CATEGORY) | Le document résultant ou un emplacement particulier dans celui-ci peut sembler légèrement différent par rapport au document original. |
| [UNEXPECTED_CONTENT](#UNEXPECTED-CONTENT) | Contenu inattendu générique, aucun code spécifique. |
| [UNEXPECTED_CONTENT_CATEGORY](#UNEXPECTED-CONTENT-CATEGORY) | Certain contenu du document source n'a pas pu être reconnu (c.-à-d. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String warningTypeName)](#fromName-java.lang.String) |  |
| [fromNames(Set warningTypeNames)](#fromNames-java.util.Set) |  |
| [getName(int warningType)](#getName-int) |  |
| [getNames(int warningType)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int warningType)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### DATA_LOSS {#DATA-LOSS}
```
public static int DATA_LOSS
```


Perte de données générique, aucun code spécifique.

### DATA_LOSS_CATEGORY {#DATA-LOSS-CATEGORY}
```
public static int DATA_LOSS_CATEGORY
```


Du texte/caractère/image ou d'autres données seront manquants soit dans l'arbre du document après le chargement, soit dans le document créé après l'enregistrement.

### FONT_EMBEDDING {#FONT-EMBEDDING}
```
public static int FONT_EMBEDDING
```


Perte d'informations de police incorporées lors de l'enregistrement du document.

### FONT_SUBSTITUTION {#FONT-SUBSTITUTION}
```
public static int FONT_SUBSTITUTION
```


La police a été substituée.

### HINT {#HINT}
```
public static int HINT
```


Avertit d'un problème potentiel ou suggère une amélioration.

### MAJOR_FORMATTING_LOSS {#MAJOR-FORMATTING-LOSS}
```
public static int MAJOR_FORMATTING_LOSS
```


Perte de mise en forme majeure générique, aucun code spécifique.

### MAJOR_FORMATTING_LOSS_CATEGORY {#MAJOR-FORMATTING-LOSS-CATEGORY}
```
public static int MAJOR_FORMATTING_LOSS_CATEGORY
```


Le document résultant ou un emplacement particulier dans celui-ci peut sembler sensiblement différent par rapport au document original.

### MINOR_FORMATTING_LOSS {#MINOR-FORMATTING-LOSS}
```
public static int MINOR_FORMATTING_LOSS
```


Perte de mise en forme mineure générique, aucun code spécifique.

### MINOR_FORMATTING_LOSS_CATEGORY {#MINOR-FORMATTING-LOSS-CATEGORY}
```
public static int MINOR_FORMATTING_LOSS_CATEGORY
```


Le document résultant ou un emplacement particulier dans celui-ci peut sembler légèrement différent par rapport au document original.

### UNEXPECTED_CONTENT {#UNEXPECTED-CONTENT}
```
public static int UNEXPECTED_CONTENT
```


Contenu inattendu générique, aucun code spécifique.

### UNEXPECTED_CONTENT_CATEGORY {#UNEXPECTED-CONTENT-CATEGORY}
```
public static int UNEXPECTED_CONTENT_CATEGORY
```


Certain contenu du document source n'a pas pu être reconnu (c.-à-d. n'est pas pris en charge), cela peut ou non causer des problèmes ou entraîner une perte de données/de mise en forme.

### length {#length}
```
public static int length
```


### fromName(String warningTypeName) {#fromName-java.lang.String}
```
public static int fromName(String warningTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| warningTypeName | java.lang.String |  |

**Returns:**
int
### fromNames(Set warningTypeNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set warningTypeNames)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| warningTypeNames | java.util.Set |  |

**Returns:**
int
### getName(int warningType) {#getName-int}
```
public static String getName(int warningType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| warningType | int |  |

**Returns:**
java.lang.String
### getNames(int warningType) {#getNames-int}
```
public static Set getNames(int warningType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| warningType | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int warningType) {#toString-int}
```
public static String toString(int warningType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| warningType | int |  |

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
