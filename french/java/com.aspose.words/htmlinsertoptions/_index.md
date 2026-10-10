---
title: "HtmlInsertOptions"
linktitle: "HtmlInsertOptions"
second_title: "Aspose.Words pour Java"
description: "Spécifie les options pour la méthode MAspose.Words.DocumentBuilder.InsertHtmlSystem.StringAspose.Words.HtmlInsertOptions en Java."
type: docs
weight: 381
url: /fr/java/com.aspose.words/htmlinsertoptions/
---

**Inheritance:**
java.lang.Object
```
public class HtmlInsertOptions
```

Spécifie les options pour la méthode **M:Aspose.Words.DocumentBuilder.InsertHtml(System.String,Aspose.Words.HtmlInsertOptions)**.

 **Examples:** 

Montre comment permettre une meilleure préservation des bordures et des marges visibles.

```

 final String HTML = "\n                \n                    \n                    \n                        paragraph 1\n                        paragraph 2\n                    \n                    \n                ";

 // Set the new mode of import HTML block-level elements.
 int insertOptions = HtmlInsertOptions.PRESERVE_BLOCKS;

 DocumentBuilder builder = new DocumentBuilder();
 builder.insertHtml(HTML, insertOptions);
 builder.getDocument().save(getArtifactsDir() + "DocumentBuilder.PreserveBlocks.docx");
 
```
## Champs

| Champ | Description |
| --- | --- |
| [NONE](#NONE) | Utilisez les options par défaut lors de l'insertion de HTML. |
| [PRESERVE_BLOCKS](#PRESERVE-BLOCKS) | Conservez les propriétés des éléments de niveau bloc. |
| [REMOVE_LAST_EMPTY_PARAGRAPH](#REMOVE-LAST-EMPTY-PARAGRAPH) | Supprimez le paragraphe vide qui est normalement inséré après le HTML se terminant par un élément de niveau bloc. |
| [USE_BUILDER_FORMATTING](#USE-BUILDER-FORMATTING) | Utilisez la mise en forme de police et de paragraphe spécifiée dans [DocumentBuilder](../../com.aspose.words/documentbuilder/) comme mise en forme de base pour le texte inséré depuis le HTML. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String htmlInsertOptionsName)](#fromName-java.lang.String) |  |
| [fromNames(Set htmlInsertOptionsNames)](#fromNames-java.util.Set) |  |
| [getName(int htmlInsertOptions)](#getName-int) |  |
| [getNames(int htmlInsertOptions)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int htmlInsertOptions)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### NONE {#NONE}
```
public static int NONE
```


Utilisez les options par défaut lors de l'insertion de HTML.

### PRESERVE_BLOCKS {#PRESERVE-BLOCKS}
```
public static int PRESERVE_BLOCKS
```


Conservez les propriétés des éléments de niveau bloc.

 **Remarks:** 

Par défaut, les propriétés des blocs parents sont fusionnées et stockées sur leurs éléments enfants (c’est‑à‑dire les paragraphes ou les tableaux). Si cette option est spécifiée, les propriétés de chaque bloc sont stockées séparément dans une structure logique spéciale. En conséquence, cette option permet de mieux préserver les bordures et les marges individuelles visibles dans le document HTML et d’obtenir de meilleurs résultats de conversion. L’inconvénient est que le document résultant devient plus difficile à modifier, car les bordures et marges stockées dans la structure logique ne sont pas disponibles pour l’édition.

Seules les marges et bordures des éléments HTML 'body', 'div' et 'blockquote' sont conservées. Les propriétés de chaque élément HTML sont stockées séparément.

Si cette option est spécifiée, Aspose.Words imite le comportement de MS Word concernant l'importation des propriétés de bloc.

### REMOVE_LAST_EMPTY_PARAGRAPH {#REMOVE-LAST-EMPTY-PARAGRAPH}
```
public static int REMOVE_LAST_EMPTY_PARAGRAPH
```


Supprimez le paragraphe vide qui est normalement inséré après le HTML se terminant par un élément de niveau bloc.

 **Remarks:** 

Par défaut, [DocumentBuilder](../../com.aspose.words/documentbuilder/) veille à ce que le dernier élément de niveau bloc importé depuis le HTML soit fermé après l’importation et insère un saut de paragraphe après l’élément. Ce saut de paragraphe sépare le contenu importé du HTML du contenu du document modèle. Cependant, si un fragment HTML est inséré dans un paragraphe vide, ce saut de paragraphe créera un paragraphe vide supplémentaire. Si ce comportement est indésirable, spécifiez cette option.

### USE_BUILDER_FORMATTING {#USE-BUILDER-FORMATTING}
```
public static int USE_BUILDER_FORMATTING
```


Utilisez la mise en forme de police et de paragraphe spécifiée dans [DocumentBuilder](../../com.aspose.words/documentbuilder/) comme mise en forme de base pour le texte inséré depuis le HTML.

 **Remarks:** 

Si cette option n’est pas spécifiée, la mise en forme de [DocumentBuilder](../../com.aspose.words/documentbuilder/) est ignorée et le texte est inséré avec la mise en forme HTML par défaut. En conséquence, le texte apparaît tel qu’il est rendu dans les navigateurs.

Si cette option est spécifiée, la mise en forme du texte inséré est basée sur la mise en forme spécifiée dans [DocumentBuilder](../../com.aspose.words/documentbuilder/), et le texte apparaît comme s’il avait été inséré en utilisant [DocumentBuilder.write(java.lang.String)](../../com.aspose.words/documentbuilder/\\#write-java.lang.String).

### length {#length}
```
public static int length
```


### fromName(String htmlInsertOptionsName) {#fromName-java.lang.String}
```
public static int fromName(String htmlInsertOptionsName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| htmlInsertOptionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set htmlInsertOptionsNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set htmlInsertOptionsNames)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| htmlInsertOptionsNames | java.util.Set |  |

**Returns:**
int
### getName(int htmlInsertOptions) {#getName-int}
```
public static String getName(int htmlInsertOptions)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| htmlInsertOptions | int |  |

**Returns:**
java.lang.String
### getNames(int htmlInsertOptions) {#getNames-int}
```
public static Set getNames(int htmlInsertOptions)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| htmlInsertOptions | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int htmlInsertOptions) {#toString-int}
```
public static String toString(int htmlInsertOptions)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| htmlInsertOptions | int |  |

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
