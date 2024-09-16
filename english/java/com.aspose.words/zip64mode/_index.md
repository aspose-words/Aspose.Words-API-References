---
title: Zip64Mode
linktitle: Zip64Mode
second_title: Aspose.Words for Java
description: Specifies when to use ZIP64 format extensions for OOXML files in Java.
type: docs
weight: 697
url: /java/com.aspose.words/zip64mode/
---

**Inheritance:**
java.lang.Object
```
public class Zip64Mode
```

Specifies when to use ZIP64 format extensions for OOXML files.

 **Remarks:** 

OOXML file is a ZIP-archive that has a 4 GB (2^32 bytes) limit on uncompressed size of a file, compressed size of a file, and total size of the archive, as well as a limit of 65,535 (2^16-1) files in archive. ZIP64 format extensions increase the limits to 2^64.

 **Examples:** 

Shows how to use ZIP64 format extensions.

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
## Fields

| Field | Description |
| --- | --- |
| [ALWAYS](#ALWAYS) | Always use ZIP64 format extensions. |
| [IF_NECESSARY](#IF-NECESSARY) | If necessary use ZIP64 format extensions. |
| [NEVER](#NEVER) | Do not use ZIP64 format extensions. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String zip64ModeName)](#fromName-java.lang.String) |  |
| [getName(int zip64Mode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int zip64Mode)](#toString-int) |  |
### ALWAYS {#ALWAYS}
```
public static int ALWAYS
```


Always use ZIP64 format extensions.

### IF_NECESSARY {#IF-NECESSARY}
```
public static int IF_NECESSARY
```


If necessary use ZIP64 format extensions.

### NEVER {#NEVER}
```
public static int NEVER
```


Do not use ZIP64 format extensions.

### length {#length}
```
public static int length
```


### fromName(String zip64ModeName) {#fromName-java.lang.String}
```
public static int fromName(String zip64ModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| zip64ModeName | java.lang.String |  |

**Returns:**
int
### getName(int zip64Mode) {#getName-int}
```
public static String getName(int zip64Mode)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| zip64Mode | int |  |

**Returns:**
java.lang.String
