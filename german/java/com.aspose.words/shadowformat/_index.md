---
title: "ShadowFormat"
linktitle: "ShadowFormat"
second_title: "Aspose.Words für Java"
description: "Stellt die Schattenformatierung für ein Objekt in Java dar."
type: docs
weight: 610
url: /de/java/com.aspose.words/shadowformat/
---

**Inheritance:**
java.lang.Object
```
public class ShadowFormat
```

Stellt Schattierungsformatierung für ein Objekt dar.

Weitere Informationen finden Sie im Dokumentationsartikel [ Working with Graphic Elements ][Working with Graphic Elements].

 **Examples:** 

Zeigt, wie man die Schattenfarbe erhält.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```


[Working with Graphic Elements]: https://docs.aspose.com/words/java/working-with-graphic-elements/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [clear()](#clear) | Löscht die Schattenformatierung. |
| [getColor()](#getColor) | Gibt ein java.awt.Color‑Objekt zurück, das die Farbe des Schattens darstellt. |
| [getTransparency()](#getTransparency) | Gibt den Transparenzgrad des Schatteneffekts als Wert zwischen 0,0 (undurchsichtig) und 1,0 (klar) zurück. |
| [getType()](#getType) | Gibt den angegebenen [ShadowType](../../com.aspose.words/shadowtype/) für ShadowFormat zurück. |
| [getVisible()](#getVisible) | Gibt  true  zurück, wenn die auf diese Instanz angewendete Formatierung sichtbar ist. |
| [setColor(Color value)](#setColor-java.awt.Color) | Setzt ein java.awt.Color‑Objekt, das die Farbe des Schattens darstellt. |
| [setTransparency(double value)](#setTransparency-double) | Legt den Transparenzgrad für den Schatteneffekt als Wert zwischen 0.0 (undurchsichtig) und 1.0 (klar) fest. |
| [setType(int value)](#setType-int) | Legt den angegebenen [ShadowType](../../com.aspose.words/shadowtype/) für ShadowFormat fest. |
### clear() {#clear}
```
public void clear()
```


Löscht die Schattenformatierung.

 **Examples:** 

Zeigt, wie man mit einer Schattenformatierung für die Form arbeitet.

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


Gibt ein java.awt.Color-Objekt zurück, das die Farbe für den Schatten darstellt. Der Standardwert ist java.awt.Color\#getBlack().getBlack().

 **Examples:** 

Zeigt, wie man die Schattenfarbe erhält.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```

Zeigt, wie man eine Farbe mit Transparenz festlegt.

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
java.awt.Color – Ein java.awt.Color-Objekt, das die Farbe für den Schatten darstellt.
### getTransparency() {#getTransparency}
```
public double getTransparency()
```


Gibt den Transparenzgrad für den Schatteneffekt als Wert zwischen 0.0 (undurchsichtig) und 1.0 (klar) zurück. Der Standardwert ist 0.0.

 **Examples:** 

Zeigt, wie man eine Farbe mit Transparenz festlegt.

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
double – Der Transparenzgrad für den Schatteneffekt als Wert zwischen 0.0 (undurchsichtig) und 1.0 (klar).
### getType() {#getType}
```
public int getType()
```


Gibt den angegebenen [ShadowType](../../com.aspose.words/shadowtype/) für ShadowFormat zurück.

 **Remarks:** 

Das Festlegen eines neuen Schattentyps setzt die Werte für Farbe und Transparenz auf ihre Standardwerte zurück. Daher ist es sinnvoll, zuerst den gewünschten Schattentyp festzulegen und erst danach die Werte für Farbe und Transparenz zu setzen.

 **Examples:** 

Zeigt, wie man die Schattenfarbe erhält.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```

**Returns:**
int – Der angegebene [ShadowType](../../com.aspose.words/shadowtype/) für ShadowFormat. Der zurückgegebene Wert ist einer der [ShadowType](../../com.aspose.words/shadowtype/) Konstanten.
### getVisible() {#getVisible}
```
public boolean getVisible()
```


Gibt  true  zurück, wenn die auf diese Instanz angewendete Formatierung sichtbar ist.

 **Remarks:** 

Im Gegensatz zu [clear()](../../com.aspose.words/shadowformat/\#clear) löscht das Zuweisen von  false  zu Visible nicht die Formatierung, sondern blendet nur den Formeffekt aus.

 **Examples:** 

Zeigt, wie man mit einer Schattenformatierung für die Form arbeitet.

```

 Document doc = new Document(getMyDir() + "Shape stroke pattern border.docx");
 Shape shape = (Shape)doc.getChildNodes(NodeType.SHAPE, true).get(0);

 if (shape.getShadowFormat().getVisible() && shape.getShadowFormat().getType() == ShadowType.SHADOW_2)
     shape.getShadowFormat().setType(ShadowType.SHADOW_7);

 if (shape.getShadowFormat().getType() == ShadowType.SHADOW_MIXED)
     shape.getShadowFormat().clear();
 
```

**Returns:**
boolean –  true  wenn die auf diese Instanz angewendete Formatierung sichtbar ist.
### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Legt ein java.awt.Color-Objekt fest, das die Farbe für den Schatten darstellt. Der Standardwert ist java.awt.Color\#getBlack().getBlack().

 **Examples:** 

Zeigt, wie man die Schattenfarbe erhält.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```

Zeigt, wie man eine Farbe mit Transparenz festlegt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.awt.Color | Ein java.awt.Color-Objekt, das die Farbe für den Schatten darstellt. |

### setTransparency(double value) {#setTransparency-double}
```
public void setTransparency(double value)
```


Legt den Transparenzgrad für den Schatteneffekt als Wert zwischen 0.0 (undurchsichtig) und 1.0 (klar) fest. Der Standardwert ist 0.0.

 **Examples:** 

Zeigt, wie man eine Farbe mit Transparenz festlegt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Der Transparenzgrad für den Schatteneffekt als Wert zwischen 0.0 (undurchsichtig) und 1.0 (klar). |

### setType(int value) {#setType-int}
```
public void setType(int value)
```


Legt den angegebenen [ShadowType](../../com.aspose.words/shadowtype/) für ShadowFormat fest.

 **Remarks:** 

Das Festlegen eines neuen Schattentyps setzt die Werte für Farbe und Transparenz auf ihre Standardwerte zurück. Daher ist es sinnvoll, zuerst den gewünschten Schattentyp festzulegen und erst danach die Werte für Farbe und Transparenz zu setzen.

 **Examples:** 

Zeigt, wie man die Schattenfarbe erhält.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der angegebene [ShadowType](../../com.aspose.words/shadowtype/) für ShadowFormat. Der Wert muss einer der [ShadowType](../../com.aspose.words/shadowtype/) Konstanten sein. |

