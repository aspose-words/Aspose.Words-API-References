---
title: "ViewType"
linktitle: "ViewType"
second_title: "Aspose.Words pour Java"
description: "Valeurs possibles pour le mode d’affichage dans Microsoft Word en Java."
type: docs
weight: 715
url: /fr/java/com.aspose.words/viewtype/
---

**Inheritance:**
java.lang.Object
```
public class ViewType
```

Valeurs possibles pour le mode d'affichage dans Microsoft Word.

 **Examples:** 

Montre comment définir un facteur de zoom personnalisé, que les versions antérieures de Microsoft Word appliqueront à un document lors du chargement.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.getViewOptions().setViewType(ViewType.PAGE_LAYOUT);
 doc.getViewOptions().setZoomPercent(50);

 Assert.assertEquals(ZoomType.CUSTOM, doc.getViewOptions().getZoomType());
 Assert.assertEquals(ZoomType.NONE, doc.getViewOptions().getZoomType());

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomPercentage.doc");
 
```
## Champs

| Champ | Description |
| --- | --- |
| [NONE](#NONE) | Le document doit être rendu dans la vue par défaut de l’application. |
| [NORMAL](#NORMAL) | Le document doit être rendu dans une vue optimisée pour le plan ou la création de documents longs. |
| [OUTLINE](#OUTLINE) | Le document doit être rendu dans une vue optimisée pour le plan ou la création de documents longs. |
| [PAGE_LAYOUT](#PAGE-LAYOUT) | Le document doit être ouvert dans une vue qui affiche le document tel qu’il sera imprimé. |
| [READING](#READING) | Le document doit être rendu dans la vue par défaut de l’application. |
| [WEB](#WEB) | Le document doit être rendu dans une vue imitant la façon dont ce document serait affiché dans une page web. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String viewTypeName)](#fromName-java.lang.String) |  |
| [getName(int viewType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int viewType)](#toString-int) |  |
### NONE {#NONE}
```
public static int NONE
```


Le document doit être rendu dans la vue par défaut de l’application.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Le document doit être rendu dans une vue optimisée pour le plan ou la création de documents longs.

### OUTLINE {#OUTLINE}
```
public static int OUTLINE
```


Le document doit être rendu dans une vue optimisée pour le plan ou la création de documents longs.

### PAGE_LAYOUT {#PAGE-LAYOUT}
```
public static int PAGE_LAYOUT
```


Le document doit être ouvert dans une vue qui affiche le document tel qu’il sera imprimé.

### READING {#READING}
```
public static int READING
```


Le document doit être rendu dans la vue par défaut de l’application.

### WEB {#WEB}
```
public static int WEB
```


Le document doit être rendu dans une vue imitant la façon dont ce document serait affiché dans une page web.

### length {#length}
```
public static int length
```


### fromName(String viewTypeName) {#fromName-java.lang.String}
```
public static int fromName(String viewTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| viewTypeName | java.lang.String |  |

**Returns:**
int
### getName(int viewType) {#getName-int}
```
public static String getName(int viewType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| viewType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int viewType) {#toString-int}
```
public static String toString(int viewType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| viewType | int |  |

**Returns:**
java.lang.String
