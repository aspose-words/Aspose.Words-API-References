---
title: "ShadowFormat"
linktitle: "ShadowFormat"
second_title: "Aspose.Words pour Java"
description: "Représente le format d'ombre pour un objet en Java."
type: docs
weight: 610
url: /fr/java/com.aspose.words/shadowformat/
---

**Inheritance:**
java.lang.Object
```
public class ShadowFormat
```

Représente le format d'ombre pour un objet.

Pour en savoir plus, consultez l'article de documentation [ Working with Graphic Elements ][Working with Graphic Elements].

 **Examples:** 

Montre comment obtenir la couleur de l'ombre.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```


[Working with Graphic Elements]: https://docs.aspose.com/words/java/working-with-graphic-elements/
## Méthodes

| Méthode | Description |
| --- | --- |
| [clear()](#clear) | Efface le format d'ombre. |
| [getColor()](#getColor) | Obtient un objet java.awt.Color qui représente la couleur de l'ombre. |
| [getTransparency()](#getTransparency) | Obtient le degré de transparence de l'effet d'ombre sous forme d'une valeur comprise entre 0,0 (opaque) et 1,0 (transparent). |
| [getType()](#getType) | Obtient le [ShadowType](../../com.aspose.words/shadowtype/) spécifié pour ShadowFormat. |
| [getVisible()](#getVisible) | Renvoie  true  si le formatage appliqué à cette instance est visible. |
| [setColor(Color value)](#setColor-java.awt.Color) | Définit un objet java.awt.Color qui représente la couleur de l'ombre. |
| [setTransparency(double value)](#setTransparency-double) | Définit le degré de transparence de l'effet d'ombre comme une valeur comprise entre 0.0 (opaque) et 1.0 (transparent). |
| [setType(int value)](#setType-int) | Définit le [ShadowType](../../com.aspose.words/shadowtype/) spécifié pour ShadowFormat. |
### clear() {#clear}
```
public void clear()
```


Efface le format d'ombre.

 **Examples:** 

Montre comment travailler avec le formatage d'ombre pour la forme.

```

 Document doc = new Document(getMyDir() + "Shape stroke pattern border.docx");
 Shape shape = (Shape)doc.getChildNodes(NodeType.SHAPE, true).get(0);

 if (shape.getShadowFormat().getVisible() && shape.getShadowFormat().getType() == ShadowType.SHADOW_2)
     shape.getShadowFormat().setType(ShadowType.SHADOW_7);

 if (shape.getShadowFormat().getType() == ShadowType.SHADOW_MIXED)
     shape.getShadowFormat().clear();
 
```

### getColor() {#getColor}
```
public Color getColor()
```


Obtient un objet java.awt.Color qui représente la couleur de l'ombre. La valeur par défaut est java.awt.Color\\#getBlack().getBlack().

 **Examples:** 

Montre comment obtenir la couleur de l'ombre.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```

Montre comment définir une couleur avec transparence.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 ShadowFormat shadowFormat = shape.getShadowFormat();
 shadowFormat.setType(ShadowType.SHADOW_21);
 shadowFormat.setColor(Color.RED);
 shadowFormat.setTransparency(0.8);

 doc.save(getArtifactsDir() + "Shape.ShadowFormatTransparency.docx");
 
```

**Returns:**
java.awt.Color - Un objet java.awt.Color qui représente la couleur de l'ombre.
### getTransparency() {#getTransparency}
```
public double getTransparency()
```


Obtient le degré de transparence de l'effet d'ombre comme une valeur comprise entre 0.0 (opaque) et 1.0 (transparent). La valeur par défaut est 0.0.

 **Examples:** 

Montre comment définir une couleur avec transparence.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 ShadowFormat shadowFormat = shape.getShadowFormat();
 shadowFormat.setType(ShadowType.SHADOW_21);
 shadowFormat.setColor(Color.RED);
 shadowFormat.setTransparency(0.8);

 doc.save(getArtifactsDir() + "Shape.ShadowFormatTransparency.docx");
 
```

**Returns:**
double - Le degré de transparence de l'effet d'ombre comme une valeur comprise entre 0.0 (opaque) et 1.0 (transparent).
### getType() {#getType}
```
public int getType()
```


Obtient le [ShadowType](../../com.aspose.words/shadowtype/) spécifié pour ShadowFormat.

 **Remarks:** 

Définir un nouveau type d'ombre réinitialisera les valeurs Color et Transparency à leurs valeurs par défaut. Il est donc logique de définir d'abord le type d'ombre souhaité, puis uniquement les valeurs Color et Transparency.

 **Examples:** 

Montre comment obtenir la couleur de l'ombre.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```

**Returns:**
int - Le [ShadowType](../../com.aspose.words/shadowtype/) spécifié pour ShadowFormat. La valeur retournée est l'une des constantes [ShadowType](../../com.aspose.words/shadowtype/).
### getVisible() {#getVisible}
```
public boolean getVisible()
```


Renvoie  true  si le formatage appliqué à cette instance est visible.

 **Remarks:** 

Contrairement à [clear()](../../com.aspose.words/shadowformat/\\#clear), affecter  false  à Visible ne supprime pas le formatage, il masque uniquement l'effet de forme.

 **Examples:** 

Montre comment travailler avec le formatage d'ombre pour la forme.

```

 Document doc = new Document(getMyDir() + "Shape stroke pattern border.docx");
 Shape shape = (Shape)doc.getChildNodes(NodeType.SHAPE, true).get(0);

 if (shape.getShadowFormat().getVisible() && shape.getShadowFormat().getType() == ShadowType.SHADOW_2)
     shape.getShadowFormat().setType(ShadowType.SHADOW_7);

 if (shape.getShadowFormat().getType() == ShadowType.SHADOW_MIXED)
     shape.getShadowFormat().clear();
 
```

**Returns:**
boolean -  true  si le formatage appliqué à cette instance est visible.
### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Définit un objet java.awt.Color qui représente la couleur de l'ombre. La valeur par défaut est java.awt.Color\\#getBlack().getBlack().

 **Examples:** 

Montre comment obtenir la couleur de l'ombre.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```

Montre comment définir une couleur avec transparence.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 ShadowFormat shadowFormat = shape.getShadowFormat();
 shadowFormat.setType(ShadowType.SHADOW_21);
 shadowFormat.setColor(Color.RED);
 shadowFormat.setTransparency(0.8);

 doc.save(getArtifactsDir() + "Shape.ShadowFormatTransparency.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.awt.Color | Un objet java.awt.Color qui représente la couleur de l'ombre. |

### setTransparency(double value) {#setTransparency-double}
```
public void setTransparency(double value)
```


Définit le degré de transparence de l'effet d'ombre comme une valeur comprise entre 0.0 (opaque) et 1.0 (transparent). La valeur par défaut est 0.0.

 **Examples:** 

Montre comment définir une couleur avec transparence.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 ShadowFormat shadowFormat = shape.getShadowFormat();
 shadowFormat.setType(ShadowType.SHADOW_21);
 shadowFormat.setColor(Color.RED);
 shadowFormat.setTransparency(0.8);

 doc.save(getArtifactsDir() + "Shape.ShadowFormatTransparency.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | Le degré de transparence de l'effet d'ombre comme une valeur comprise entre 0.0 (opaque) et 1.0 (transparent). |

### setType(int value) {#setType-int}
```
public void setType(int value)
```


Définit le [ShadowType](../../com.aspose.words/shadowtype/) spécifié pour ShadowFormat.

 **Remarks:** 

Définir un nouveau type d'ombre réinitialisera les valeurs Color et Transparency à leurs valeurs par défaut. Il est donc logique de définir d'abord le type d'ombre souhaité, puis uniquement les valeurs Color et Transparency.

 **Examples:** 

Montre comment obtenir la couleur de l'ombre.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | Le [ShadowType](../../com.aspose.words/shadowtype/) spécifié pour ShadowFormat. La valeur doit être l'une des constantes [ShadowType](../../com.aspose.words/shadowtype/). |

