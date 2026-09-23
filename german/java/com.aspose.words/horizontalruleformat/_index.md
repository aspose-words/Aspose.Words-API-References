---
title: "HorizontalRuleFormat"
linktitle: "HorizontalRuleFormat"
second_title: "Aspose.Words für Java"
description: "Stellt die Formatierung einer horizontalen Linie in Java dar."
type: docs
weight: 376
url: /de/java/com.aspose.words/horizontalruleformat/
---

**Inheritance:**
java.lang.Object
```
public class HorizontalRuleFormat
```

Stellt die Formatierung der horizontalen Linie dar.

Um mehr zu erfahren, besuchen Sie den [ Working with Shapes ][Working with Shapes] Dokumentationsartikel.

 **Examples:** 

Zeigt, wie man eine horizontale Regel‑Form einfügt und deren Formatierung anpasst.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getAlignment()](#getAlignment) | Ermittelt die Ausrichtung der horizontalen Linie. |
| [getColor()](#getColor) | Ermittelt die Pinsel‑Farbe, die die horizontale Linie füllt. |
| [getHeight()](#getHeight) | Ermittelt die Höhe der horizontalen Linie. |
| [getNoShade()](#getNoShade) | Gibt an, ob eine 3D‑Schattierung für die horizontale Linie vorhanden ist. |
| [getWidthPercent()](#getWidthPercent) | Ermittelt die Länge der angegebenen horizontalen Linie, ausgedrückt als Prozentsatz der Fensterbreite. |
| [setAlignment(int value)](#setAlignment-int) | Setzt die Ausrichtung der horizontalen Linie. |
| [setColor(Color value)](#setColor-java.awt.Color) | Setzt die Pinsel‑Farbe, die die horizontale Regel füllt. |
| [setHeight(double value)](#setHeight-double) | Setzt die Höhe der horizontalen Regel. |
| [setNoShade(boolean value)](#setNoShade-boolean) | Gibt an, ob eine 3D‑Schattierung für die horizontale Linie vorhanden ist. |
| [setWidthPercent(double value)](#setWidthPercent-double) | Setzt die Länge der angegebenen horizontalen Regel, ausgedrückt als Prozentsatz der Fensterbreite. |
### getAlignment() {#getAlignment}
```
public int getAlignment()
```


Ermittelt die Ausrichtung der horizontalen Linie.

 **Remarks:** 

Der Standardwert ist [HorizontalRuleAlignment.LEFT](../../com.aspose.words/horizontalrulealignment/\#LEFT).

 **Examples:** 

Zeigt, wie man eine horizontale Regel‑Form einfügt und deren Formatierung anpasst.

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
int - Die Ausrichtung der horizontalen Regel. Der zurückgegebene Wert ist einer der [HorizontalRuleAlignment](../../com.aspose.words/horizontalrulealignment/) Konstanten.
### getColor() {#getColor}
```
public Color getColor()
```


Ermittelt die Pinsel‑Farbe, die die horizontale Linie füllt.

 **Remarks:** 

Dies ist eine Abkürzung zur [Fill.getColor()](../../com.aspose.words/fill/\#getColor) / [Fill.setColor(java.awt.Color)](../../com.aspose.words/fill/\#setColor-java.awt.Color) Eigenschaft.

Der Standardwert ist java.awt.Color\#getGray().getGray().

 **Examples:** 

Zeigt, wie man eine horizontale Regel‑Form einfügt und deren Formatierung anpasst.

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
java.awt.Color - Die Pinsel‑Farbe, die die horizontale Regel füllt.
### getHeight() {#getHeight}
```
public double getHeight()
```


Ermittelt die Höhe der horizontalen Linie.

**Returns:**
double - Die Höhe der horizontalen Regel.
### getNoShade() {#getNoShade}
```
public boolean getNoShade()
```


Gibt an, ob für die horizontale Regel 3D‑Schattierung vorhanden ist. Wenn  true , dann ist die horizontale Regel ohne 3D‑Schattierung und es wird eine einfarbige Farbe verwendet.

 **Remarks:** 

Der Standardwert ist  false .

 **Examples:** 

Zeigt, wie man eine horizontale Regel‑Form einfügt und deren Formatierung anpasst.

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
boolean - Der entsprechende  boolean  Wert.
### getWidthPercent() {#getWidthPercent}
```
public double getWidthPercent()
```


Ermittelt die Länge der angegebenen horizontalen Linie, ausgedrückt als Prozentsatz der Fensterbreite.

**Returns:**
double - Die Länge der angegebenen horizontalen Regel, ausgedrückt als Prozentsatz der Fensterbreite.
### setAlignment(int value) {#setAlignment-int}
```
public void setAlignment(int value)
```


Setzt die Ausrichtung der horizontalen Linie.

 **Remarks:** 

Der Standardwert ist [HorizontalRuleAlignment.LEFT](../../com.aspose.words/horizontalrulealignment/\#LEFT).

 **Examples:** 

Zeigt, wie man eine horizontale Regel‑Form einfügt und deren Formatierung anpasst.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Die Ausrichtung der horizontalen Regel. Der Wert muss einer der [HorizontalRuleAlignment](../../com.aspose.words/horizontalrulealignment/) Konstanten sein. |

### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Setzt die Pinsel‑Farbe, die die horizontale Regel füllt.

 **Remarks:** 

Dies ist eine Abkürzung zur [Fill.getColor()](../../com.aspose.words/fill/\#getColor) / [Fill.setColor(java.awt.Color)](../../com.aspose.words/fill/\#setColor-java.awt.Color) Eigenschaft.

Der Standardwert ist java.awt.Color\#getGray().getGray().

 **Examples:** 

Zeigt, wie man eine horizontale Regel‑Form einfügt und deren Formatierung anpasst.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.awt.Color | Die Pinsel‑Farbe, die die horizontale Regel füllt. |

### setHeight(double value) {#setHeight-double}
```
public void setHeight(double value)
```


Setzt die Höhe der horizontalen Regel.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Die Höhe der horizontalen Regel. |

### setNoShade(boolean value) {#setNoShade-boolean}
```
public void setNoShade(boolean value)
```


Gibt an, ob für die horizontale Regel 3D‑Schattierung vorhanden ist. Wenn  true , dann ist die horizontale Regel ohne 3D‑Schattierung und es wird eine einfarbige Farbe verwendet.

 **Remarks:** 

Der Standardwert ist  false .

 **Examples:** 

Zeigt, wie man eine horizontale Regel‑Form einfügt und deren Formatierung anpasst.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setWidthPercent(double value) {#setWidthPercent-double}
```
public void setWidthPercent(double value)
```


Setzt die Länge der angegebenen horizontalen Regel, ausgedrückt als Prozentsatz der Fensterbreite.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Die Länge der angegebenen horizontalen Regel, ausgedrückt als Prozentsatz der Fensterbreite. |

