---
title: "MultiPageLayout"
linktitle: "MultiPageLayout"
second_title: "Aspose.Words pour Java"
description: "Définit une mise en page pour rendre plusieurs pages en une seule sortie en Java."
type: docs
weight: 472
url: /fr/java/com.aspose.words/multipagelayout/
---

**Inheritance:**
java.lang.Object
```
public class MultiPageLayout
```

Définit une mise en page pour le rendu de plusieurs pages en une seule sortie.

 **Remarks:** 

Utilisez l'une des méthodes d'usine statiques pour créer une configuration de mise en page.

 **Examples:** 

Montre comment enregistrer le document en image JPG avec les paramètres de mise en page multi-pages.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.JPEG);
 // Set up a grid layout with:
 // - 3 columns per row.
 // - 10pts spacing between pages (horizontal and vertical).
 options.setPageLayout(MultiPageLayout.grid(3, 10f, 10f));

 // Alternative layouts:
 // options.PageLayout = MultiPageLayout.Horizontal(10);
 // options.PageLayout = MultiPageLayout.Vertical(10);

 // Customize the background and border.
 options.getPageLayout().setBackColor(Color.lightGray);
 options.getPageLayout().setBorderColor(Color.BLUE);
 options.getPageLayout().setBorderWidth(2f);

 doc.save(getArtifactsDir() + "ImageSaveOptions.GridLayout.jpg", options);
 
```
## Méthodes

| Méthode | Description |
| --- | --- |
| [getBackColor()](#getBackColor) | Obtient la couleur d'arrière-plan de la sortie. |
| [getBorderColor()](#getBorderColor) | Obtient la couleur de la bordure des pages. |
| [getBorderWidth()](#getBorderWidth) | Obtient la largeur de la bordure des pages. |
| [grid(int columns, float horizontalGap, float verticalGap)](#grid-int-float-float) | Crée une mise en page où les pages sont rendues de gauche à droite, de haut en bas, dans une grille avec le nombre de colonnes spécifié. |
| [horizontal(float horizontalGap)](#horizontal-float) | Crée une mise en page où toutes les pages spécifiées sont rendues horizontalement côte à côte, de gauche à droite, dans une seule sortie. |
| [setBackColor(Color value)](#setBackColor-java.awt.Color) | Définit la couleur d'arrière-plan de la sortie. |
| [setBorderColor(Color value)](#setBorderColor-java.awt.Color) | Définit la couleur de la bordure des pages. |
| [setBorderWidth(float value)](#setBorderWidth-float) | Définit la largeur de la bordure des pages. |
| [singlePage()](#singlePage) | Crée une mise en page qui rend uniquement la première des pages spécifiées. |
| [tiffFrames()](#tiffFrames) | Crée une mise en page où chaque page est rendue comme une trame séparée dans une image TIFF multi-trames. |
| [vertical(float verticalGap)](#vertical-float) | Crée une mise en page où toutes les pages spécifiées sont rendues verticalement, l'une sous l'autre, dans une seule sortie. |
### getBackColor() {#getBackColor}
```
public Color getBackColor()
```


Obtient la couleur d'arrière-plan de la sortie. La valeur par défaut est java.awt.Color\#EMPTY.EMPTY.

**Returns:**
java.awt.Color - La couleur d'arrière-plan de la sortie.
### getBorderColor() {#getBorderColor}
```
public Color getBorderColor()
```


Obtient la couleur de la bordure des pages. La valeur par défaut est java.awt.Color\#EMPTY.EMPTY.

**Returns:**
java.awt.Color - La couleur de la bordure des pages.
### getBorderWidth() {#getBorderWidth}
```
public float getBorderWidth()
```


Obtient la largeur de la bordure des pages. La valeur par défaut est 0.

**Returns:**
float - La largeur de la bordure des pages.
### grid(int columns, float horizontalGap, float verticalGap) {#grid-int-float-float}
```
public static MultiPageLayout grid(int columns, float horizontalGap, float verticalGap)
```


Crée une mise en page où les pages sont rendues de gauche à droite, de haut en bas, dans une grille avec le nombre de colonnes spécifié.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| colonnes | int | Le nombre de colonnes dans la mise en page. Doit être supérieur à zéro. |
| horizontalGap | float | L'écart horizontal entre les colonnes en points. |
| verticalGap | float | L'écart vertical entre les lignes en points. |

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
### horizontal(float horizontalGap) {#horizontal-float}
```
public static MultiPageLayout horizontal(float horizontalGap)
```


Crée une mise en page où toutes les pages spécifiées sont rendues horizontalement côte à côte, de gauche à droite, dans une seule sortie.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| horizontalGap | float | L'écart horizontal entre les pages en points. |

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
### setBackColor(Color value) {#setBackColor-java.awt.Color}
```
public void setBackColor(Color value)
```


Définit la couleur d'arrière-plan de la sortie. La valeur par défaut est java.awt.Color\#EMPTY.EMPTY.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.awt.Color | La couleur d'arrière-plan de la sortie. |

### setBorderColor(Color value) {#setBorderColor-java.awt.Color}
```
public void setBorderColor(Color value)
```


Définit la couleur de la bordure des pages. La valeur par défaut est java.awt.Color\#EMPTY.EMPTY.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.awt.Color | La couleur de la bordure des pages. |

### setBorderWidth(float value) {#setBorderWidth-float}
```
public void setBorderWidth(float value)
```


Définit la largeur de la bordure des pages. La valeur par défaut est 0.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | float | La largeur de la bordure des pages. |

### singlePage() {#singlePage}
```
public static MultiPageLayout singlePage()
```


Crée une mise en page qui rend uniquement la première des pages spécifiées.

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
### tiffFrames() {#tiffFrames}
```
public static MultiPageLayout tiffFrames()
```


Crée une mise en page où chaque page est rendue comme une trame séparée dans une image TIFF multi-trames. Applicable uniquement aux formats d'image TIFF.

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
### vertical(float verticalGap) {#vertical-float}
```
public static MultiPageLayout vertical(float verticalGap)
```


Crée une mise en page où toutes les pages spécifiées sont rendues verticalement, l'une sous l'autre, dans une seule sortie.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| verticalGap | float | L'écart vertical entre les pages en points. |

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
