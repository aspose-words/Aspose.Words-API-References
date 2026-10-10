---
title: "Zip64Mode"
linktitle: "Zip64Mode"
second_title: "Aspose.Words Java için"
description: "Java'da OOXML dosyaları için ZIP64 format uzantılarının ne zaman kullanılacağını belirtir."
type: docs
weight: 750
url: /tr/java/com.aspose.words/zip64mode/
---

**Inheritance:**
java.lang.Object
```
public class Zip64Mode
```

OOXML dosyaları için ZIP64 format uzantılarının ne zaman kullanılacağını belirtir.

 **Remarks:** 

OOXML dosyası, bir dosyanın sıkıştırılmamış boyutu, sıkıştırılmış boyutu ve arşivin toplam boyutu için 4 GB (2^32 bayt) ve arşivdeki dosya sayısı için 65.535 (2^16-1) sınırlaması olan bir ZIP arşividir. ZIP64 format uzantıları bu sınırlamaları 2^64'e yükseltir.

 **Examples:** 

ZIP64 format uzantılarının nasıl kullanılacağını gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [ALWAYS](#ALWAYS) | Her zaman ZIP64 format uzantılarını kullan. |
| [IF_NECESSARY](#IF-NECESSARY) | Gerekirse ZIP64 format uzantılarını kullan. |
| [NEVER](#NEVER) | ZIP64 format uzantılarını kullanma. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String zip64ModeName)](#fromName-java.lang.String) |  |
| [getName(int zip64Mode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int zip64Mode)](#toString-int) |  |
### ALWAYS {#ALWAYS}
```
public static int ALWAYS
```


Her zaman ZIP64 format uzantılarını kullan.

### IF_NECESSARY {#IF-NECESSARY}
```
public static int IF_NECESSARY
```


Gerekirse ZIP64 format uzantılarını kullan.

### NEVER {#NEVER}
```
public static int NEVER
```


ZIP64 format uzantılarını kullanma.

### length {#length}
```
public static int length
```


### fromName(String zip64ModeName) {#fromName-java.lang.String}
```
public static int fromName(String zip64ModeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| zip64ModeName | java.lang.String |  |

**Returns:**
int
### getName(int zip64Mode) {#getName-int}
```
public static String getName(int zip64Mode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| zip64Mode | int |  |

**Returns:**
java.lang.String
