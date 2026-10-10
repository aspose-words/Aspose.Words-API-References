---
title: "MergeFormatMode"
linktitle: "MergeFormatMode"
second_title: "Aspose.Words Java için"
description: "Java'da birden fazla belge birleştirildiğinde biçimlendirmenin nasıl birleştirileceğini belirtir."
type: docs
weight: 464
url: /tr/java/com.aspose.words/mergeformatmode/
---

**Inheritance:**
java.lang.Object
```
public class MergeFormatMode
```

Birden fazla belge birleştirildiğinde biçimlendirmelerin nasıl birleştirildiğini belirtir.

 **Examples:** 

Belgeleri tek bir çıkış belgesine nasıl birleştireceğinizi gösterir.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.1.docx", new String[]{inputDoc1, inputDoc2});

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.2.docx", new String[]{inputDoc1, inputDoc2}, saveOptions, MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.3.pdf", new String[]{inputDoc1, inputDoc2}, SaveFormat.PDF, MergeFormatMode.KEEP_SOURCE_LAYOUT);

 LoadOptions firstLoadOptions = new LoadOptions();
 {
     firstLoadOptions.setIgnoreOleData(true);
 }
 LoadOptions secondLoadOptions = new LoadOptions();
 {
     secondLoadOptions.setIgnoreOleData(false);
 }
 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.4.docx", new String[]{inputDoc1, inputDoc2}, new LoadOptions[]{firstLoadOptions, secondLoadOptions},
         saveOptions, MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Document doc = Merger.merge(new String[]{inputDoc1, inputDoc2}, MergeFormatMode.MERGE_FORMATTING);
 doc.save(getArtifactsDir() + "LowCode.MergeDocument.5.docx");

 doc = Merger.merge(new String[]{inputDoc1, inputDoc2}, new LoadOptions[]{firstLoadOptions, secondLoadOptions}, MergeFormatMode.MERGE_FORMATTING);
 doc.save(getArtifactsDir() + "LowCode.MergeDocument.6.docx");
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [KEEP_SOURCE_FORMATTING](#KEEP-SOURCE-FORMATTING) | Kaynak belgenin, içeriklerine uygulanan yazı tipi stilleri, boyutları, renkleri, girintileri ve diğer tüm biçimlendirme öğeleri gibi özgün biçimlendirmesini koruyacağı anlamına gelir. |
| [KEEP_SOURCE_LAYOUT](#KEEP-SOURCE-LAYOUT) | Orijinal belgelerin düzenini son belgede koruyun. |
| [MERGE_FORMATTING](#MERGE-FORMATTING) | Birleştirilen belgelerin biçimlendirmesini birleştirin. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String mergeFormatModeName)](#fromName-java.lang.String) |  |
| [getName(int mergeFormatMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int mergeFormatMode)](#toString-int) |  |
### KEEP_SOURCE_FORMATTING {#KEEP-SOURCE-FORMATTING}
```
public static int KEEP_SOURCE_FORMATTING
```


Kaynak belgenin, içeriklerine uygulanan yazı tipi stilleri, boyutları, renkleri, girintileri ve diğer tüm biçimlendirme öğeleri gibi özgün biçimlendirmesini koruyacağı anlamına gelir.

 **Remarks:** 

Bu seçeneği kullanarak, birleştirme kuyruğundaki ilk belgenin biçimlendirme ayarlarından bağımsız olarak, kopyalanan içeriğin özgün kaynaktaki gibi görünmesini sağlarsınız.

Girdi ve çıktı formatları PDF olduğunda bu seçeneğin hiçbir etkisi yoktur.

### KEEP_SOURCE_LAYOUT {#KEEP-SOURCE-LAYOUT}
```
public static int KEEP_SOURCE_LAYOUT
```


Orijinal belgelerin düzenini son belgede koruyun.

 **Remarks:** 

Genel olarak, orijinal belgeleri yazdırıp yapıştırıcıyla manuel olarak birleştiriyormuş gibi görünür.

### MERGE_FORMATTING {#MERGE-FORMATTING}
```
public static int MERGE_FORMATTING
```


Birleştirilen belgelerin biçimlendirmesini birleştirin.

 **Remarks:** 

Bu seçeneği kullanarak, Aspose.Words ilk belgenin biçimlendirmesini ikinci belgenin yapısı ve görünümüyle eşleşecek şekilde uyarlarken, bazı özgün biçimlendirmeleri olduğu gibi tutar. Bu seçenek, hedef belgenin genel görünüm ve hissini korumak istediğinizde ancak özgün belgeden belirli biçimlendirme öğelerini de saklamak istediğinizde faydalıdır.

Girdi ve çıktı formatları PDF olduğunda bu seçeneğin hiçbir etkisi yoktur.

### length {#length}
```
public static int length
```


### fromName(String mergeFormatModeName) {#fromName-java.lang.String}
```
public static int fromName(String mergeFormatModeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| mergeFormatModeName | java.lang.String |  |

**Returns:**
int
### getName(int mergeFormatMode) {#getName-int}
```
public static String getName(int mergeFormatMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| mergeFormatMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int mergeFormatMode) {#toString-int}
```
public static String toString(int mergeFormatMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| mergeFormatMode | int |  |

**Returns:**
java.lang.String
