---
title: "Zip64Mode"
linktitle: "Zip64Mode"
second_title: "Aspose.Words para Java"
description: "Especifica cuándo usar extensiones de formato ZIP64 para archivos OOXML en Java."
type: docs
weight: 750
url: /es/java/com.aspose.words/zip64mode/
---

**Inheritance:**
java.lang.Object
```
public class Zip64Mode
```

Especifica cuándo usar extensiones de formato ZIP64 para archivos OOXML.

 **Remarks:** 

Un archivo OOXML es un archivo ZIP que tiene un límite de 4 GB (2^32 bytes) en el tamaño sin comprimir de un archivo, el tamaño comprimido de un archivo y el tamaño total del archivo, así como un límite de 65 535 (2^16‑1) archivos en el archivo. Las extensiones de formato ZIP64 aumentan los límites a 2^64.

 **Examples:** 

Muestra cómo usar extensiones de formato ZIP64.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [ALWAYS](#ALWAYS) | Utilice siempre extensiones de formato ZIP64. |
| [IF_NECESSARY](#IF-NECESSARY) | Si es necesario, use extensiones de formato ZIP64. |
| [NEVER](#NEVER) | No use extensiones de formato ZIP64. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String zip64ModeName)](#fromName-java.lang.String) |  |
| [getName(int zip64Mode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int zip64Mode)](#toString-int) |  |
### ALWAYS {#ALWAYS}
```
public static int ALWAYS
```


Utilice siempre extensiones de formato ZIP64.

### IF_NECESSARY {#IF-NECESSARY}
```
public static int IF_NECESSARY
```


Si es necesario, use extensiones de formato ZIP64.

### NEVER {#NEVER}
```
public static int NEVER
```


No use extensiones de formato ZIP64.

### length {#length}
```
public static int length
```


### fromName(String zip64ModeName) {#fromName-java.lang.String}
```
public static int fromName(String zip64ModeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| zip64ModeName | java.lang.String |  |

**Returns:**
int
### getName(int zip64Mode) {#getName-int}
```
public static String getName(int zip64Mode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| zip64Mode | int |  |

**Returns:**
java.lang.String
