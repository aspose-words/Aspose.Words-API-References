---
title: "ShadowFormat"
linktitle: "ShadowFormat"
second_title: "Aspose.Words per Java"
description: "Rappresenta la formattazione dell'ombra per un oggetto in Java."
type: docs
weight: 610
url: /it/java/com.aspose.words/shadowformat/
---

**Inheritance:**
java.lang.Object
```
public class ShadowFormat
```

Rappresenta la formattazione dell'ombra per un oggetto.

Per saperne di più, visita l'articolo di documentazione [ Lavorare con gli Elementi Grafici ][Working with Graphic Elements].

 **Examples:** 

Mostra come ottenere il colore dell'ombra.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```


[Working with Graphic Elements]: https://docs.aspose.com/words/java/working-with-graphic-elements/
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [clear()](#clear) | Cancella la formattazione dell'ombra. |
| [getColor()](#getColor) | Ottiene un oggetto java.awt.Color che rappresenta il colore dell'ombra. |
| [getTransparency()](#getTransparency) | Ottiene il grado di trasparenza dell'effetto ombra come valore compreso tra 0,0 (opaco) e 1,0 (chiaro). |
| [getType()](#getType) | Ottiene il [ShadowType](../../com.aspose.words/shadowtype/) specificato per ShadowFormat. |
| [getVisible()](#getVisible) | Restituisce  true  se la formattazione applicata a questa istanza è visibile. |
| [setColor(Color value)](#setColor-java.awt.Color) | Imposta un oggetto java.awt.Color che rappresenta il colore dell'ombra. |
| [setTransparency(double value)](#setTransparency-double) | Imposta il grado di trasparenza per l'effetto ombra come valore compreso tra 0.0 (opaco) e 1.0 (trasparente). |
| [setType(int value)](#setType-int) | Imposta il [ShadowType](../../com.aspose.words/shadowtype/) specificato per ShadowFormat. |
### clear() {#clear}
```
public void clear()
```


Cancella la formattazione dell'ombra.

 **Examples:** 

Mostra come lavorare con la formattazione dell'ombra per la forma.

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


Ottiene un oggetto java.awt.Color che rappresenta il colore dell'ombra. Il valore predefinito è java.awt.Color\#getBlack().getBlack().

 **Examples:** 

Mostra come ottenere il colore dell'ombra.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```

Mostra come impostare un colore con trasparenza.

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
java.awt.Color - Un oggetto java.awt.Color che rappresenta il colore dell'ombra.
### getTransparency() {#getTransparency}
```
public double getTransparency()
```


Ottiene il grado di trasparenza per l'effetto ombra come valore compreso tra 0.0 (opaco) e 1.0 (trasparente). Il valore predefinito è 0.0.

 **Examples:** 

Mostra come impostare un colore con trasparenza.

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
double - Il grado di trasparenza per l'effetto ombra come valore compreso tra 0.0 (opaco) e 1.0 (trasparente).
### getType() {#getType}
```
public int getType()
```


Ottiene il [ShadowType](../../com.aspose.words/shadowtype/) specificato per ShadowFormat.

 **Remarks:** 

Impostare un nuovo tipo di ombra ripristinerà i valori di Color e Transparency ai loro valori predefiniti. Pertanto, ha senso impostare prima il tipo di ombra desiderato e solo successivamente i valori di Color e Transparency.

 **Examples:** 

Mostra come ottenere il colore dell'ombra.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```

**Returns:**
int - Il [ShadowType](../../com.aspose.words/shadowtype/) specificato per ShadowFormat. Il valore restituito è una delle costanti [ShadowType](../../com.aspose.words/shadowtype/).
### getVisible() {#getVisible}
```
public boolean getVisible()
```


Restituisce  true  se la formattazione applicata a questa istanza è visibile.

 **Remarks:** 

A differenza di [clear()](../../com.aspose.words/shadowformat/\#clear), assegnare  false  a Visible non cancella la formattazione, ma nasconde solo l'effetto della forma.

 **Examples:** 

Mostra come lavorare con la formattazione dell'ombra per la forma.

```

 Document doc = new Document(getMyDir() + "Shape stroke pattern border.docx");
 Shape shape = (Shape)doc.getChildNodes(NodeType.SHAPE, true).get(0);

 if (shape.getShadowFormat().getVisible() && shape.getShadowFormat().getType() == ShadowType.SHADOW_2)
     shape.getShadowFormat().setType(ShadowType.SHADOW_7);

 if (shape.getShadowFormat().getType() == ShadowType.SHADOW_MIXED)
     shape.getShadowFormat().clear();
 
```

**Returns:**
boolean -  true  se la formattazione applicata a questa istanza è visibile.
### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Imposta un oggetto java.awt.Color che rappresenta il colore dell'ombra. Il valore predefinito è java.awt.Color\#getBlack().getBlack().

 **Examples:** 

Mostra come ottenere il colore dell'ombra.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```

Mostra come impostare un colore con trasparenza.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.awt.Color | Un oggetto java.awt.Color che rappresenta il colore dell'ombra. |

### setTransparency(double value) {#setTransparency-double}
```
public void setTransparency(double value)
```


Imposta il grado di trasparenza per l'effetto ombra come valore compreso tra 0.0 (opaco) e 1.0 (trasparente). Il valore predefinito è 0.0.

 **Examples:** 

Mostra come impostare un colore con trasparenza.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | Il grado di trasparenza per l'effetto ombra come valore compreso tra 0.0 (opaco) e 1.0 (trasparente). |

### setType(int value) {#setType-int}
```
public void setType(int value)
```


Imposta il [ShadowType](../../com.aspose.words/shadowtype/) specificato per ShadowFormat.

 **Remarks:** 

Impostare un nuovo tipo di ombra ripristinerà i valori di Color e Transparency ai loro valori predefiniti. Pertanto, ha senso impostare prima il tipo di ombra desiderato e solo successivamente i valori di Color e Transparency.

 **Examples:** 

Mostra come ottenere il colore dell'ombra.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il [ShadowType](../../com.aspose.words/shadowtype/) specificato per ShadowFormat. Il valore deve essere una delle costanti [ShadowType](../../com.aspose.words/shadowtype/). |

