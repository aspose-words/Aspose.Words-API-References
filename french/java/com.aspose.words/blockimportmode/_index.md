---
title: "BlockImportMode"
linktitle: "BlockImportMode"
second_title: "Aspose.Words pour Java"
description: "Spécifie comment les propriétés des éléments de niveau bloc sont importées à partir de documents basés sur HTML en Java."
type: docs
weight: 39
url: /fr/java/com.aspose.words/blockimportmode/
---

**Inheritance:**
java.lang.Object
```
public class BlockImportMode
```

Spécifie comment les propriétés des éléments de niveau bloc sont importées depuis des documents basés sur HTML.

 **Examples:** 

Montre comment les propriétés des éléments de niveau bloc sont importées à partir de documents basés sur HTML.

```

 final String html = "\n\n \n \n paragraph 1\n paragraph 2\n\n\n";

 HtmlLoadOptions loadOptions = new HtmlLoadOptions();
 // Set the new mode of import HTML block-level elements.
 loadOptions.setBlockImportMode(blockImportMode);

 Document doc = new Document(new ByteArrayInputStream(html.getBytes(StandardCharsets.UTF_8)), loadOptions);
 doc.save(getArtifactsDir() + "HtmlLoadOptions.BlockImport.docx");
 
```
## Champs

| Champ | Description |
| --- | --- |
| [MERGE](#MERGE) | Les propriétés des blocs parents sont fusionnées et stockées sur les éléments enfants (c.-à-d. |
| [PRESERVE](#PRESERVE) | Les propriétés des blocs parents sont importées dans une structure logique spéciale et sont stockées séparément des nœuds du document. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String blockImportModeName)](#fromName-java.lang.String) |  |
| [getName(int blockImportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int blockImportMode)](#toString-int) |  |
### MERGE {#MERGE}
```
public static int MERGE
```


Les propriétés des blocs parents sont fusionnées et stockées sur les éléments enfants (c.-à-d. paragraphes ou tableaux).

 **Remarks:** 

Les propriétés des blocs parents sont fusionnées comme suit : les marges sont additionnées ; les bordures des blocs de niveau supérieur sont supprimées et seules les bordures du niveau le plus interne sont conservées. En conséquence, lorsque ce mode est spécifié, une partie du formatage des blocs du document original sera perdue.

D'autre part, comme toutes les propriétés de niveau bloc fusionnées sont stockées sur les nœuds du document, tout le formatage du document résultant sera disponible pour modification.

### PRESERVE {#PRESERVE}
```
public static int PRESERVE
```


Les propriétés des blocs parents sont importées dans une structure logique spéciale et sont stockées séparément des nœuds du document.

 **Remarks:** 

Seules les marges et bordures des éléments HTML 'body', 'div' et 'blockquote' sont importées. Les propriétés de chaque élément HTML sont stockées individuellement.

Ce mode permet de mieux préserver les bordures et marges visibles dans le document HTML et d'obtenir de meilleurs résultats de conversion. L'inconvénient est que le document résultant devient plus difficile à modifier, car les bordures et marges stockées dans la structure logique ne sont pas disponibles pour l'édition.

Ce mode imite le comportement de MS Word concernant l'importation des propriétés de bloc.

### length {#length}
```
public static int length
```


### fromName(String blockImportModeName) {#fromName-java.lang.String}
```
public static int fromName(String blockImportModeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| blockImportModeName | java.lang.String |  |

**Returns:**
int
### getName(int blockImportMode) {#getName-int}
```
public static String getName(int blockImportMode)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| blockImportMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int blockImportMode) {#toString-int}
```
public static String toString(int blockImportMode)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| blockImportMode | int |  |

**Returns:**
java.lang.String
