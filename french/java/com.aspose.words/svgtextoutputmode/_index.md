---
title: "SvgTextOutputMode"
linktitle: "SvgTextOutputMode"
second_title: "Aspose.Words pour Java"
description: "Permet de spécifier comment le texte d'un document doit être rendu lors de l'enregistrement au format SVG en Java."
type: docs
weight: 650
url: /fr/java/com.aspose.words/svgtextoutputmode/
---

**Inheritance:**
java.lang.Object
```
public class SvgTextOutputMode
```

Permet de spécifier comment le texte à l'intérieur d'un document doit être rendu lors de l'enregistrement au format SVG.

 **Examples:** 

Montre comment imiter les propriétés des images lors de la conversion d'un document .docx en .svg.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 // Configure the SvgSaveOptions object to save with no page borders or selectable text.
 SvgSaveOptions options = new SvgSaveOptions();
 {
     options.setFitToViewPort(true);
     options.setShowPageBorder(false);
     options.setTextOutputMode(SvgTextOutputMode.USE_PLACED_GLYPHS);
 }

 doc.save(getArtifactsDir() + "SvgSaveOptions.SaveLikeImage.svg", options);
 
```
## Champs

| Champ | Description |
| --- | --- |
| [USE_PLACED_GLYPHS](#USE-PLACED-GLYPHS) | Le texte est rendu à l'aide de courbes. |
| [USE_SVG_FONTS](#USE-SVG-FONTS) | Des polices SVG sont utilisées pour rendre le texte. |
| [USE_TARGET_MACHINE_FONTS](#USE-TARGET-MACHINE-FONTS) | Les polices installées sur la machine cible sont utilisées pour rendre le texte. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String svgTextOutputModeName)](#fromName-java.lang.String) |  |
| [getName(int svgTextOutputMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int svgTextOutputMode)](#toString-int) |  |
### USE_PLACED_GLYPHS {#USE-PLACED-GLYPHS}
```
public static int USE_PLACED_GLYPHS
```


Le texte est rendu à l'aide de courbes. Remarque : la sélection du texte ne fonctionnera pas si vous utilisez cette option.

### USE_SVG_FONTS {#USE-SVG-FONTS}
```
public static int USE_SVG_FONTS
```


Des polices SVG sont utilisées pour rendre le texte. Remarque : tous les navigateurs ne prennent pas en charge les polices SVG.

### USE_TARGET_MACHINE_FONTS {#USE-TARGET-MACHINE-FONTS}
```
public static int USE_TARGET_MACHINE_FONTS
```


Les polices installées sur la machine cible sont utilisées pour rendre le texte. Remarque : si certaines des polices utilisées dans le document ne sont pas disponibles sur la machine cible, le document peut apparaître différemment.

### length {#length}
```
public static int length
```


### fromName(String svgTextOutputModeName) {#fromName-java.lang.String}
```
public static int fromName(String svgTextOutputModeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| svgTextOutputModeName | java.lang.String |  |

**Returns:**
int
### getName(int svgTextOutputMode) {#getName-int}
```
public static String getName(int svgTextOutputMode)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| svgTextOutputMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int svgTextOutputMode) {#toString-int}
```
public static String toString(int svgTextOutputMode)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| svgTextOutputMode | int |  |

**Returns:**
java.lang.String
