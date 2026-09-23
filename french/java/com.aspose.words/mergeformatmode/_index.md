---
title: "MergeFormatMode"
linktitle: "MergeFormatMode"
second_title: "Aspose.Words pour Java"
description: "Spécifie comment le formatage est fusionné lors de la combinaison de plusieurs documents en Java."
type: docs
weight: 464
url: /fr/java/com.aspose.words/mergeformatmode/
---

**Inheritance:**
java.lang.Object
```
public class MergeFormatMode
```

Spécifie comment le formatage est fusionné lors de la combinaison de plusieurs documents.

 **Examples:** 

Montre comment fusionner des documents en un seul document de sortie.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.1.docx", new String[]{inputDoc1, inputDoc2});

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.2.docx", new String[]{inputDoc1, inputDoc2}, saveOptions, MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.3.pdf", new String[]{inputDoc1, inputDoc2}, SaveFormat.PDF, MergeFormatMode.KEEP_SOURCE_LAYOUT);

 LoadOptions firstLoadOptions = new LoadOptions();
 {
     firstLoadOptions.setIgnoreOleData(true);
 }
 LoadOptions secondLoadOptions = new LoadOptions();
 {
     secondLoadOptions.setIgnoreOleData(false);
 }
 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.4.docx", new String[]{inputDoc1, inputDoc2}, new LoadOptions[]{firstLoadOptions, secondLoadOptions},
         saveOptions, MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Document doc = Merger.merge(new String[]{inputDoc1, inputDoc2}, MergeFormatMode.MERGE_FORMATTING);
 doc.save(getArtifactsDir() + "LowCode.MergeDocument.5.docx");

 doc = Merger.merge(new String[]{inputDoc1, inputDoc2}, new LoadOptions[]{firstLoadOptions, secondLoadOptions}, MergeFormatMode.MERGE_FORMATTING);
 doc.save(getArtifactsDir() + "LowCode.MergeDocument.6.docx");
 
```
## Champs

| Champ | Description |
| --- | --- |
| [KEEP_SOURCE_FORMATTING](#KEEP-SOURCE-FORMATTING) | Cela signifie que le document source conservera son formatage d'origine, tel que les styles de police, les tailles, les couleurs, les retraits et tout autre élément de formatage appliqué à son contenu. |
| [KEEP_SOURCE_LAYOUT](#KEEP-SOURCE-LAYOUT) | Conservez la mise en page des documents originaux dans le document final. |
| [MERGE_FORMATTING](#MERGE-FORMATTING) | Combinez le formatage des documents fusionnés. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String mergeFormatModeName)](#fromName-java.lang.String) |  |
| [getName(int mergeFormatMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int mergeFormatMode)](#toString-int) |  |
### KEEP_SOURCE_FORMATTING {#KEEP-SOURCE-FORMATTING}
```
public static int KEEP_SOURCE_FORMATTING
```


Cela signifie que le document source conservera son formatage d'origine, tel que les styles de police, les tailles, les couleurs, les retraits et tout autre élément de formatage appliqué à son contenu.

 **Remarks:** 

En utilisant cette option, vous vous assurez que le contenu copié apparaît comme dans la source originale, quel que soit le paramétrage de formatage du premier document dans la file de fusion.

Cette option n'a aucun effet lorsque les formats d'entrée et de sortie sont PDF.

### KEEP_SOURCE_LAYOUT {#KEEP-SOURCE-LAYOUT}
```
public static int KEEP_SOURCE_LAYOUT
```


Conservez la mise en page des documents originaux dans le document final.

 **Remarks:** 

En général, cela ressemble à imprimer les documents originaux et à les coller manuellement ensemble à l'aide de colle.

### MERGE_FORMATTING {#MERGE-FORMATTING}
```
public static int MERGE_FORMATTING
```


Combinez le formatage des documents fusionnés.

 **Remarks:** 

En utilisant cette option, Aspose.Words adapte le formatage du premier document pour correspondre à la structure et à l'apparence du deuxième document, tout en conservant une partie du formatage original intacte. Cette option est utile lorsque vous souhaitez préserver l'aspect général du document de destination tout en conservant certains aspects du formatage du document original.

Cette option n'a aucun effet lorsque les formats d'entrée et de sortie sont PDF.

### length {#length}
```
public static int length
```


### fromName(String mergeFormatModeName) {#fromName-java.lang.String}
```
public static int fromName(String mergeFormatModeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| mergeFormatModeName | java.lang.String |  |

**Returns:**
int
### getName(int mergeFormatMode) {#getName-int}
```
public static String getName(int mergeFormatMode)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| mergeFormatMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int mergeFormatMode) {#toString-int}
```
public static String toString(int mergeFormatMode)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| mergeFormatMode | int |  |

**Returns:**
java.lang.String
