---
title: "SvgTextOutputMode"
linktitle: "SvgTextOutputMode"
second_title: "Aspose.Words für Java"
description: "Ermöglicht die Angabe, wie Text in einem Dokument beim Speichern im SVG‑Format in Java gerendert werden soll."
type: docs
weight: 650
url: /de/java/com.aspose.words/svgtextoutputmode/
---

**Inheritance:**
java.lang.Object
```
public class SvgTextOutputMode
```

Ermöglicht die Angabe, wie Text innerhalb eines Dokuments beim Speichern im SVG-Format gerendert werden soll.

 **Examples:** 

Zeigt, wie die Eigenschaften von Bildern beim Konvertieren eines .docx‑Dokuments zu .svg nachgeahmt werden können.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [USE_PLACED_GLYPHS](#USE-PLACED-GLYPHS) | Text wird mit Kurven gerendert. |
| [USE_SVG_FONTS](#USE-SVG-FONTS) | SVG‑Schriften werden zum Rendern von Text verwendet. |
| [USE_TARGET_MACHINE_FONTS](#USE-TARGET-MACHINE-FONTS) | Auf dem Zielrechner installierte Schriften werden zum Rendern von Text verwendet. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String svgTextOutputModeName)](#fromName-java.lang.String) |  |
| [getName(int svgTextOutputMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int svgTextOutputMode)](#toString-int) |  |
### USE_PLACED_GLYPHS {#USE-PLACED-GLYPHS}
```
public static int USE_PLACED_GLYPHS
```


Text wird mit Kurven gerendert. Hinweis: Die Textauswahl funktioniert nicht, wenn Sie diese Option verwenden.

### USE_SVG_FONTS {#USE-SVG-FONTS}
```
public static int USE_SVG_FONTS
```


SVG‑Schriften werden zum Rendern von Text verwendet. Hinweis: Nicht alle Browser unterstützen SVG‑Schriften.

### USE_TARGET_MACHINE_FONTS {#USE-TARGET-MACHINE-FONTS}
```
public static int USE_TARGET_MACHINE_FONTS
```


Auf dem Zielrechner installierte Schriften werden zum Rendern von Text verwendet. Hinweis: Wenn einige der im Dokument verwendeten Schriften auf dem Zielrechner nicht verfügbar sind, kann das Dokument anders aussehen.

### length {#length}
```
public static int length
```


### fromName(String svgTextOutputModeName) {#fromName-java.lang.String}
```
public static int fromName(String svgTextOutputModeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| svgTextOutputModeName | java.lang.String |  |

**Returns:**
int
### getName(int svgTextOutputMode) {#getName-int}
```
public static String getName(int svgTextOutputMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| svgTextOutputMode | int |  |

**Returns:**
java.lang.String
