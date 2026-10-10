---
title: "MultiPageLayout"
linktitle: "MultiPageLayout"
second_title: "Aspose.Words für Java"
description: "Definiert ein Layout zum Rendern mehrerer Seiten in einer einzigen Ausgabe in Java."
type: docs
weight: 472
url: /de/java/com.aspose.words/multipagelayout/
---

**Inheritance:**
java.lang.Object
```
public class MultiPageLayout
```

Definiert ein Layout zum Rendern mehrerer Seiten in einer einzigen Ausgabe.

 **Remarks:** 

Verwenden Sie eine der statischen Fabrikmethoden, um eine Layout-Konfiguration zu erstellen.

 **Examples:** 

Zeigt, wie man das Dokument mit den Multi-Page-Layout-Einstellungen als JPG-Bild speichert.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getBackColor()](#getBackColor) | Liefert die Hintergrundfarbe der Ausgabe. |
| [getBorderColor()](#getBorderColor) | Liefert die Farbe des Seitenrandes. |
| [getBorderWidth()](#getBorderWidth) | Liefert die Breite des Seitenrandes. |
| [grid(int columns, float horizontalGap, float verticalGap)](#grid-int-float-float) | Erstellt ein Layout, bei dem Seiten von links nach rechts und von oben nach unten in einem Raster mit der angegebenen Spaltenanzahl gerendert werden. |
| [horizontal(float horizontalGap)](#horizontal-float) | Erstellt ein Layout, bei dem alle angegebenen Seiten horizontal nebeneinander von links nach rechts in einer einzigen Ausgabe gerendert werden. |
| [setBackColor(Color value)](#setBackColor-java.awt.Color) | Setzt die Hintergrundfarbe der Ausgabe. |
| [setBorderColor(Color value)](#setBorderColor-java.awt.Color) | Setzt die Farbe des Seitenrandes. |
| [setBorderWidth(float value)](#setBorderWidth-float) | Setzt die Breite des Seitenrandes. |
| [singlePage()](#singlePage) | Erstellt ein Layout, das nur die erste der angegebenen Seiten rendert. |
| [tiffFrames()](#tiffFrames) | Erstellt ein Layout, bei dem jede Seite als separates Bild in einem mehrteiligen TIFF-Bild gerendert wird. |
| [vertical(float verticalGap)](#vertical-float) | Erstellt ein Layout, bei dem alle angegebenen Seiten vertikal untereinander in einer einzigen Ausgabe gerendert werden. |
### getBackColor() {#getBackColor}
```
public Color getBackColor()
```


Liest die Hintergrundfarbe der Ausgabe. Der Standardwert ist java.awt.Color\#EMPTY.EMPTY.

**Returns:**
java.awt.Color - Die Hintergrundfarbe der Ausgabe.
### getBorderColor() {#getBorderColor}
```
public Color getBorderColor()
```


Liest die Farbe des Seitenrandes. Der Standardwert ist java.awt.Color\#EMPTY.EMPTY.

**Returns:**
java.awt.Color - Die Farbe des Seitenrandes.
### getBorderWidth() {#getBorderWidth}
```
public float getBorderWidth()
```


Liest die Breite des Seitenrandes. Der Standardwert ist 0.

**Returns:**
float - Die Breite des Seitenrandes.
### grid(int columns, float horizontalGap, float verticalGap) {#grid-int-float-float}
```
public static MultiPageLayout grid(int columns, float horizontalGap, float verticalGap)
```


Erstellt ein Layout, bei dem Seiten von links nach rechts und von oben nach unten in einem Raster mit der angegebenen Spaltenanzahl gerendert werden.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Spalten | int | Die Anzahl der Spalten im Layout. Muss größer als null sein. |
| horizontalGap | float | Der horizontale Abstand zwischen den Spalten in Punkten. |
| verticalGap | float | Der vertikale Abstand zwischen den Zeilen in Punkten. |

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
### horizontal(float horizontalGap) {#horizontal-float}
```
public static MultiPageLayout horizontal(float horizontalGap)
```


Erstellt ein Layout, bei dem alle angegebenen Seiten horizontal nebeneinander von links nach rechts in einer einzigen Ausgabe gerendert werden.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| horizontalGap | float | Der horizontale Abstand zwischen den Seiten in Punkten. |

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
### setBackColor(Color value) {#setBackColor-java.awt.Color}
```
public void setBackColor(Color value)
```


Setzt die Hintergrundfarbe der Ausgabe. Der Standardwert ist java.awt.Color\#EMPTY.EMPTY.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.awt.Color | Die Hintergrundfarbe der Ausgabe. |

### setBorderColor(Color value) {#setBorderColor-java.awt.Color}
```
public void setBorderColor(Color value)
```


Setzt die Farbe des Seitenrandes. Der Standardwert ist java.awt.Color\#EMPTY.EMPTY.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.awt.Color | Die Farbe des Seitenrandes. |

### setBorderWidth(float value) {#setBorderWidth-float}
```
public void setBorderWidth(float value)
```


Setzt die Breite des Seitenrandes. Der Standardwert ist 0.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | float | Die Breite des Seitenrandes. |

### singlePage() {#singlePage}
```
public static MultiPageLayout singlePage()
```


Erstellt ein Layout, das nur die erste der angegebenen Seiten rendert.

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
### tiffFrames() {#tiffFrames}
```
public static MultiPageLayout tiffFrames()
```


Erstellt ein Layout, bei dem jede Seite als separates Bild in einem mehrteiligen TIFF-Bild gerendert wird. Nur für TIFF-Bildformate anwendbar.

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
### vertical(float verticalGap) {#vertical-float}
```
public static MultiPageLayout vertical(float verticalGap)
```


Erstellt ein Layout, bei dem alle angegebenen Seiten vertikal untereinander in einer einzigen Ausgabe gerendert werden.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| verticalGap | float | Der vertikale Abstand zwischen den Seiten in Punkten. |

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
