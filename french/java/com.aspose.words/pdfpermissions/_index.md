---
title: "PdfPermissions"
linktitle: "PdfPermissions"
second_title: "Aspose.Words pour Java"
description: "Spécifie les opérations autorisées à un utilisateur sur un document PDF chiffré en Java."
type: docs
weight: 541
url: /fr/java/com.aspose.words/pdfpermissions/
---

**Inheritance:**
java.lang.Object
```
public class PdfPermissions
```

Spécifie les opérations autorisées à un utilisateur sur un document PDF chiffré.

 **Examples:** 

Montre comment définir les autorisations sur un document PDF enregistré.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Extend permissions to allow the editing of annotations.
 PdfEncryptionDetails encryptionDetails =
         new PdfEncryptionDetails("password", "", PdfPermissions.MODIFY_ANNOTATIONS | PdfPermissions.DOCUMENT_ASSEMBLY);

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Enable encryption via the "EncryptionDetails" property.
 saveOptions.setEncryptionDetails(encryptionDetails);

 // When we open this document, we will need to provide the password before accessing its contents.
 doc.save(getArtifactsDir() + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
 
```
## Champs

| Champ | Description |
| --- | --- |
| [ALLOW_ALL](#ALLOW-ALL) | Autorise toutes les opérations sur le document PDF. |
| [CONTENT_COPY](#CONTENT-COPY) | Copier ou extraire autrement le texte et les graphiques du document par des opérations autres que celles contrôlées par [CONTENT\_COPY\_FOR\_ACCESSIBILITY](../../com.aspose.words/pdfpermissions/\#CONTENT-COPY-FOR-ACCESSIBILITY). |
| [CONTENT_COPY_FOR_ACCESSIBILITY](#CONTENT-COPY-FOR-ACCESSIBILITY) | Extraire le texte et les graphiques (dans le cadre de l'accessibilité pour les utilisateurs handicapés ou à d'autres fins). |
| [DISALLOW_ALL](#DISALLOW-ALL) | Interdit toutes les opérations sur le document PDF. |
| [DOCUMENT_ASSEMBLY](#DOCUMENT-ASSEMBLY) | Assembler le document (insérer, faire pivoter ou supprimer des pages et créer des éléments de plan du document ou des images miniatures), même si [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) est désactivé. |
| [FILL_IN](#FILL-IN) | Remplir les champs de formulaire interactifs existants (y compris les champs de signature), même si [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) est désactivé. |
| [HIGH_RESOLUTION_PRINTING](#HIGH-RESOLUTION-PRINTING) | Imprimer le document vers une représentation à partir de laquelle une copie numérique fidèle du contenu PDF peut être générée, selon un algorithme dépendant de l'implémentation. |
| [MODIFY_ANNOTATIONS](#MODIFY-ANNOTATIONS) | Ajouter ou modifier des annotations de texte, remplir les champs de formulaire interactifs et, si [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) est également activé, créer ou modifier des champs de formulaire interactifs (y compris les champs de signature). |
| [MODIFY_CONTENTS](#MODIFY-CONTENTS) | Modifier le contenu du document par des opérations autres que celles contrôlées par [MODIFY\_ANNOTATIONS](../../com.aspose.words/pdfpermissions/\#MODIFY-ANNOTATIONS), [FILL\_IN](../../com.aspose.words/pdfpermissions/\#FILL-IN) et [DOCUMENT\_ASSEMBLY](../../com.aspose.words/pdfpermissions/\#DOCUMENT-ASSEMBLY). |
| [PRINTING](#PRINTING) | Imprimer le document (possiblement pas au niveau de qualité le plus élevé, selon que [HIGH\_RESOLUTION\_PRINTING](../../com.aspose.words/pdfpermissions/\#HIGH-RESOLUTION-PRINTING) est également activé). |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String pdfPermissionsName)](#fromName-java.lang.String) |  |
| [fromNames(Set pdfPermissionsNames)](#fromNames-java.util.Set) |  |
| [getName(int pdfPermissions)](#getName-int) |  |
| [getNames(int pdfPermissions)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfPermissions)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### ALLOW_ALL {#ALLOW-ALL}
```
public static int ALLOW_ALL
```


Autorise toutes les opérations sur le document PDF.

### CONTENT_COPY {#CONTENT-COPY}
```
public static int CONTENT_COPY
```


Copier ou extraire autrement le texte et les graphiques du document par des opérations autres que celles contrôlées par [CONTENT\_COPY\_FOR\_ACCESSIBILITY](../../com.aspose.words/pdfpermissions/\#CONTENT-COPY-FOR-ACCESSIBILITY).

### CONTENT_COPY_FOR_ACCESSIBILITY {#CONTENT-COPY-FOR-ACCESSIBILITY}
```
public static int CONTENT_COPY_FOR_ACCESSIBILITY
```


Extraire le texte et les graphiques (dans le cadre de l'accessibilité pour les utilisateurs handicapés ou à d'autres fins).

### DISALLOW_ALL {#DISALLOW-ALL}
```
public static int DISALLOW_ALL
```


Interdit toutes les opérations sur le document PDF. C'est la valeur par défaut.

### DOCUMENT_ASSEMBLY {#DOCUMENT-ASSEMBLY}
```
public static int DOCUMENT_ASSEMBLY
```


Assembler le document (insérer, faire pivoter ou supprimer des pages et créer des éléments de plan du document ou des images miniatures), même si [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) est désactivé.

### FILL_IN {#FILL-IN}
```
public static int FILL_IN
```


Remplir les champs de formulaire interactifs existants (y compris les champs de signature), même si [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) est désactivé.

### HIGH_RESOLUTION_PRINTING {#HIGH-RESOLUTION-PRINTING}
```
public static int HIGH_RESOLUTION_PRINTING
```


Imprimer le document vers une représentation à partir de laquelle une copie numérique fidèle du contenu PDF peut être générée, selon un algorithme dépendant de l'implémentation. Lorsque ce drapeau est désactivé (et que [PRINTING](../../com.aspose.words/pdfpermissions/\#PRINTING) est activé), l'impression doit être limitée à une représentation de bas niveau de l'apparence, éventuellement de qualité dégradée.

### MODIFY_ANNOTATIONS {#MODIFY-ANNOTATIONS}
```
public static int MODIFY_ANNOTATIONS
```


Ajouter ou modifier des annotations de texte, remplir les champs de formulaire interactifs et, si [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) est également activé, créer ou modifier des champs de formulaire interactifs (y compris les champs de signature).

### MODIFY_CONTENTS {#MODIFY-CONTENTS}
```
public static int MODIFY_CONTENTS
```


Modifier le contenu du document par des opérations autres que celles contrôlées par [MODIFY\_ANNOTATIONS](../../com.aspose.words/pdfpermissions/\#MODIFY-ANNOTATIONS), [FILL\_IN](../../com.aspose.words/pdfpermissions/\#FILL-IN) et [DOCUMENT\_ASSEMBLY](../../com.aspose.words/pdfpermissions/\#DOCUMENT-ASSEMBLY).

### PRINTING {#PRINTING}
```
public static int PRINTING
```


Imprimer le document (possiblement pas au niveau de qualité le plus élevé, selon que [HIGH\_RESOLUTION\_PRINTING](../../com.aspose.words/pdfpermissions/\#HIGH-RESOLUTION-PRINTING) est également activé).

### length {#length}
```
public static int length
```


### fromName(String pdfPermissionsName) {#fromName-java.lang.String}
```
public static int fromName(String pdfPermissionsName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| pdfPermissionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set pdfPermissionsNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set pdfPermissionsNames)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| pdfPermissionsNames | java.util.Set |  |

**Returns:**
int
### getName(int pdfPermissions) {#getName-int}
```
public static String getName(int pdfPermissions)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| pdfPermissions | int |  |

**Returns:**
java.lang.String
### getNames(int pdfPermissions) {#getNames-int}
```
public static Set getNames(int pdfPermissions)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| pdfPermissions | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pdfPermissions) {#toString-int}
```
public static String toString(int pdfPermissions)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| pdfPermissions | int |  |

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
