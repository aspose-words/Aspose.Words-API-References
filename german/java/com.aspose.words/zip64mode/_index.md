---
title: "Zip64Mode"
linktitle: "Zip64Mode"
second_title: "Aspose.Words für Java"
description: "Gibt an, wann ZIP64-Formatserweiterungen für OOXML-Dateien in Java verwendet werden sollen."
type: docs
weight: 750
url: /de/java/com.aspose.words/zip64mode/
---

**Inheritance:**
java.lang.Object
```
public class Zip64Mode
```

Gibt an, wann ZIP64-Format-Erweiterungen für OOXML-Dateien verwendet werden sollen.

 **Remarks:** 

Eine OOXML-Datei ist ein ZIP-Archiv, das eine Grenze von 4 GB (2^32 Bytes) für die unkomprimierte Dateigröße, die komprimierte Dateigröße und die Gesamtgröße des Archivs hat, sowie eine Grenze von 65 535 (2^16‑1) Dateien im Archiv. ZIP64-Formatserweiterungen erhöhen die Grenzen auf 2^64.

 **Examples:** 

Zeigt, wie ZIP64-Formatserweiterungen verwendet werden.

```

 Random random = new Random();
 DocumentBuilder builder = new DocumentBuilder();

 for (int i = 0; i < 10000; i++)
 {
     BufferedImage bmp = new BufferedImage(5, 5, BufferedImage.TYPE_INT_ARGB);
     Graphics2D g = bmp.createGraphics();
     g.setColor(new Color(random.nextInt(254), random.nextInt(254), random.nextInt(254)));
     g.drawImage(bmp, 0, 0, null);
     g.dispose();
     builder.insertImage(bmp);
 }

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 saveOptions.setZip64Mode(Zip64Mode.ALWAYS);

 builder.getDocument().save(getArtifactsDir() + "OoxmlSaveOptions.Zip64ModeOption.docx", saveOptions);
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [ALWAYS](#ALWAYS) | Verwenden Sie immer ZIP64-Formatserweiterungen. |
| [IF_NECESSARY](#IF-NECESSARY) | Verwenden Sie bei Bedarf ZIP64-Formatserweiterungen. |
| [NEVER](#NEVER) | Verwenden Sie keine ZIP64-Formatserweiterungen. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String zip64ModeName)](#fromName-java.lang.String) |  |
| [getName(int zip64Mode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int zip64Mode)](#toString-int) |  |
### ALWAYS {#ALWAYS}
```
public static int ALWAYS
```


Verwenden Sie immer ZIP64-Formatserweiterungen.

### IF_NECESSARY {#IF-NECESSARY}
```
public static int IF_NECESSARY
```


Verwenden Sie bei Bedarf ZIP64-Formatserweiterungen.

### NEVER {#NEVER}
```
public static int NEVER
```


Verwenden Sie keine ZIP64-Formatserweiterungen.

### length {#length}
```
public static int length
```


### fromName(String zip64ModeName) {#fromName-java.lang.String}
```
public static int fromName(String zip64ModeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| zip64ModeName | java.lang.String |  |

**Returns:**
int
### getName(int zip64Mode) {#getName-int}
```
public static String getName(int zip64Mode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| zip64Mode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int zip64Mode) {#toString-int}
```
public static String toString(int zip64Mode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| zip64Mode | int |  |

**Returns:**
java.lang.String
