---
title: "HorizontalRuleFormat"
linktitle: "HorizontalRuleFormat"
second_title: "Aspose.Words pour Java"
description: "Représente le formatage de la règle horizontale en Java."
type: docs
weight: 376
url: /fr/java/com.aspose.words/horizontalruleformat/
---

**Inheritance:**
java.lang.Object
```
public class HorizontalRuleFormat
```

Représente le formatage de la règle horizontale.

Pour en savoir plus, consultez l'article de documentation [ Working with Shapes ][Working with Shapes].

 **Examples:** 

Montre comment insérer une forme de règle horizontale et personnaliser son formatage.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```


[Working with Shapes]: https://docs.aspose.com/words/java/working-with-shapes/
## Méthodes

| Méthode | Description |
| --- | --- |
| [getAlignment()](#getAlignment) | Obtient l'alignement de la règle horizontale. |
| [getColor()](#getColor) | Obtient la couleur du pinceau qui remplit la règle horizontale. |
| [getHeight()](#getHeight) | Obtient la hauteur de la règle horizontale. |
| [getNoShade()](#getNoShade) | Indique la présence d'un ombrage 3D pour la règle horizontale. |
| [getWidthPercent()](#getWidthPercent) | Obtient la longueur de la règle horizontale spécifiée exprimée en pourcentage de la largeur de la fenêtre. |
| [setAlignment(int value)](#setAlignment-int) | Définit l'alignement de la règle horizontale. |
| [setColor(Color value)](#setColor-java.awt.Color) | Définit la couleur du pinceau qui remplit la règle horizontale. |
| [setHeight(double value)](#setHeight-double) | Définit la hauteur de la règle horizontale. |
| [setNoShade(boolean value)](#setNoShade-boolean) | Indique la présence d'un ombrage 3D pour la règle horizontale. |
| [setWidthPercent(double value)](#setWidthPercent-double) | Définit la longueur de la règle horizontale spécifiée exprimée en pourcentage de la largeur de la fenêtre. |
### getAlignment() {#getAlignment}
```
public int getAlignment()
```


Obtient l'alignement de la règle horizontale.

 **Remarks:** 

La valeur par défaut est [HorizontalRuleAlignment.LEFT](../../com.aspose.words/horizontalrulealignment/\#LEFT).

 **Examples:** 

Montre comment insérer une forme de règle horizontale et personnaliser son formatage.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Returns:**
int - L'alignement de la règle horizontale. La valeur renvoyée est l'une des constantes [HorizontalRuleAlignment](../../com.aspose.words/horizontalrulealignment/).
### getColor() {#getColor}
```
public Color getColor()
```


Obtient la couleur du pinceau qui remplit la règle horizontale.

 **Remarks:** 

Ceci est un raccourci vers la propriété [Fill.getColor()](../../com.aspose.words/fill/\#getColor) / [Fill.setColor(java.awt.Color)](../../com.aspose.words/fill/\#setColor-java.awt.Color).

La valeur par défaut est java.awt.Color\#getGray().getGray().

 **Examples:** 

Montre comment insérer une forme de règle horizontale et personnaliser son formatage.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Returns:**
java.awt.Color - La couleur du pinceau qui remplit la règle horizontale.
### getHeight() {#getHeight}
```
public double getHeight()
```


Obtient la hauteur de la règle horizontale.

**Returns:**
double - La hauteur de la règle horizontale.
### getNoShade() {#getNoShade}
```
public boolean getNoShade()
```


Indique la présence d'un ombrage 3D pour la règle horizontale. Si  true , alors la règle horizontale n'a pas d'ombrage 3D et une couleur unie est utilisée.

 **Remarks:** 

La valeur par défaut est false.

 **Examples:** 

Montre comment insérer une forme de règle horizontale et personnaliser son formatage.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Returns:**
boolean - La valeur  boolean  correspondante.
### getWidthPercent() {#getWidthPercent}
```
public double getWidthPercent()
```


Obtient la longueur de la règle horizontale spécifiée exprimée en pourcentage de la largeur de la fenêtre.

**Returns:**
double - La longueur de la règle horizontale spécifiée exprimée en pourcentage de la largeur de la fenêtre.
### setAlignment(int value) {#setAlignment-int}
```
public void setAlignment(int value)
```


Définit l'alignement de la règle horizontale.

 **Remarks:** 

La valeur par défaut est [HorizontalRuleAlignment.LEFT](../../com.aspose.words/horizontalrulealignment/\#LEFT).

 **Examples:** 

Montre comment insérer une forme de règle horizontale et personnaliser son formatage.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | L'alignement de la règle horizontale. La valeur doit être l'une des constantes [HorizontalRuleAlignment](../../com.aspose.words/horizontalrulealignment/). |

### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Définit la couleur du pinceau qui remplit la règle horizontale.

 **Remarks:** 

Ceci est un raccourci vers la propriété [Fill.getColor()](../../com.aspose.words/fill/\#getColor) / [Fill.setColor(java.awt.Color)](../../com.aspose.words/fill/\#setColor-java.awt.Color).

La valeur par défaut est java.awt.Color\#getGray().getGray().

 **Examples:** 

Montre comment insérer une forme de règle horizontale et personnaliser son formatage.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.awt.Color | La couleur du pinceau qui remplit la règle horizontale. |

### setHeight(double value) {#setHeight-double}
```
public void setHeight(double value)
```


Définit la hauteur de la règle horizontale.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | La hauteur de la règle horizontale. |

### setNoShade(boolean value) {#setNoShade-boolean}
```
public void setNoShade(boolean value)
```


Indique la présence d'un ombrage 3D pour la règle horizontale. Si  true , alors la règle horizontale n'a pas d'ombrage 3D et une couleur unie est utilisée.

 **Remarks:** 

La valeur par défaut est false.

 **Examples:** 

Montre comment insérer une forme de règle horizontale et personnaliser son formatage.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setWidthPercent(double value) {#setWidthPercent-double}
```
public void setWidthPercent(double value)
```


Définit la longueur de la règle horizontale spécifiée exprimée en pourcentage de la largeur de la fenêtre.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | La longueur de la règle horizontale spécifiée exprimée en pourcentage de la largeur de la fenêtre. |

