---
title: "ZoomType"
linktitle: "ZoomType"
second_title: "Aspose.Words pour Java"
description: "Valeurs possibles pour la taille d’affichage du document à l’écran dans Microsoft Word en Java."
type: docs
weight: 751
url: /fr/java/com.aspose.words/zoomtype/
---

**Inheritance:**
java.lang.Object
```
public class ZoomType
```

Valeurs possibles pour la taille d'affichage du document à l'écran dans Microsoft Word.

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
| [CUSTOM](#CUSTOM) | Le pourcentage de zoom est défini explicitement. |
| [FULL_PAGE](#FULL-PAGE) | Le pourcentage de zoom est automatiquement recalculé pour ajuster une page complète. |
| [NONE](#NONE) | Indique d’utiliser le pourcentage de zoom explicite. |
| [PAGE_WIDTH](#PAGE-WIDTH) | Le pourcentage de zoom est automatiquement recalculé pour ajuster la largeur de la page. |
| [TEXT_FIT](#TEXT-FIT) | Le pourcentage de zoom est automatiquement recalculé pour ajuster le texte. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String zoomTypeName)](#fromName-java.lang.String) |  |
| [getName(int zoomType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int zoomType)](#toString-int) |  |
### CUSTOM {#CUSTOM}
```
public static int CUSTOM
```


Le pourcentage de zoom est défini explicitement. Il n’est pas recalculé automatiquement lorsque la taille du contrôle change.

### FULL_PAGE {#FULL-PAGE}
```
public static int FULL_PAGE
```


Le pourcentage de zoom est automatiquement recalculé pour ajuster une page complète.

### NONE {#NONE}
```
public static int NONE
```


Indique d’utiliser le pourcentage de zoom explicite. Identique à [CUSTOM](../../com.aspose.words/zoomtype/\\#CUSTOM).

### PAGE_WIDTH {#PAGE-WIDTH}
```
public static int PAGE_WIDTH
```


Le pourcentage de zoom est automatiquement recalculé pour ajuster la largeur de la page.

### TEXT_FIT {#TEXT-FIT}
```
public static int TEXT_FIT
```


Le pourcentage de zoom est automatiquement recalculé pour ajuster le texte.

### length {#length}
```
public static int length
```


### fromName(String zoomTypeName) {#fromName-java.lang.String}
```
public static int fromName(String zoomTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| zoomTypeName | java.lang.String |  |

**Returns:**
int
### getName(int zoomType) {#getName-int}
```
public static String getName(int zoomType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| zoomType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int zoomType) {#toString-int}
```
public static String toString(int zoomType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| zoomType | int |  |

**Returns:**
java.lang.String
