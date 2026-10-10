---
title: "Zip64Mode"
linktitle: "Zip64Mode"
second_title: "Aspose.Words per Java"
description: "Specifica quando utilizzare le estensioni del formato ZIP64 per i file OOXML in Java."
type: docs
weight: 750
url: /it/java/com.aspose.words/zip64mode/
---

**Inheritance:**
java.lang.Object
```
public class Zip64Mode
```

Specifica quando utilizzare le estensioni del formato ZIP64 per i file OOXML.

 **Remarks:** 

Il file OOXML è un archivio ZIP che ha un limite di 4 GB (2^32 byte) sulla dimensione non compressa di un file, sulla dimensione compressa di un file e sulla dimensione totale dell'archivio, oltre a un limite di 65.535 (2^16‑1) file nell'archivio. Le estensioni del formato ZIP64 aumentano i limiti a 2^64.

 **Examples:** 

Mostra come utilizzare le estensioni del formato ZIP64.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [ALWAYS](#ALWAYS) | Utilizza sempre le estensioni del formato ZIP64. |
| [IF_NECESSARY](#IF-NECESSARY) | Se necessario, utilizza le estensioni del formato ZIP64. |
| [NEVER](#NEVER) | Non utilizzare le estensioni del formato ZIP64. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String zip64ModeName)](#fromName-java.lang.String) |  |
| [getName(int zip64Mode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int zip64Mode)](#toString-int) |  |
### ALWAYS {#ALWAYS}
```
public static int ALWAYS
```


Utilizza sempre le estensioni del formato ZIP64.

### IF_NECESSARY {#IF-NECESSARY}
```
public static int IF_NECESSARY
```


Se necessario, utilizza le estensioni del formato ZIP64.

### NEVER {#NEVER}
```
public static int NEVER
```


Non utilizzare le estensioni del formato ZIP64.

### length {#length}
```
public static int length
```


### fromName(String zip64ModeName) {#fromName-java.lang.String}
```
public static int fromName(String zip64ModeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| zip64ModeName | java.lang.String |  |

**Returns:**
int
### getName(int zip64Mode) {#getName-int}
```
public static String getName(int zip64Mode)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| zip64Mode | int |  |

**Returns:**
java.lang.String
