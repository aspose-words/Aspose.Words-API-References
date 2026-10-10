---
title: "BlockImportMode"
linktitle: "BlockImportMode"
second_title: "Aspose.Words Java için"
description: "Java'da HTML tabanlı belgelerden blok düzeyindeki öğelerin özelliklerinin nasıl içe aktarıldığını belirtir."
type: docs
weight: 39
url: /tr/java/com.aspose.words/blockimportmode/
---

**Inheritance:**
java.lang.Object
```
public class BlockImportMode
```

Blok düzeyindeki öğelerin özelliklerinin HTML tabanlı belgelerden nasıl içe aktarıldığını belirtir.

 **Examples:** 

Blok düzeyindeki öğelerin özelliklerinin HTML tabanlı belgelerden nasıl içe aktarıldığını gösterir.

```

 final String html = "\n\n \n \n paragraph 1\n paragraph 2\n\n\n";

 HtmlLoadOptions loadOptions = new HtmlLoadOptions();
 // Set the new mode of import HTML block-level elements.
 loadOptions.setBlockImportMode(blockImportMode);

 Document doc = new Document(new ByteArrayInputStream(html.getBytes(StandardCharsets.UTF_8)), loadOptions);
 doc.save(getArtifactsDir() + "HtmlLoadOptions.BlockImport.docx");
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [MERGE](#MERGE) | Üst blokların özellikleri birleştirilir ve alt öğelere (örneğin |
| [PRESERVE](#PRESERVE) | Üst blokların özellikleri özel bir mantıksal yapıya aktarılır ve belge düğümlerinden ayrı olarak depolanır. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String blockImportModeName)](#fromName-java.lang.String) |  |
| [getName(int blockImportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int blockImportMode)](#toString-int) |  |
### MERGE {#MERGE}
```
public static int MERGE
```


Üst blokların özellikleri birleştirilir ve alt öğelere (örneğin paragraflar veya tablolar) depolanır.

 **Remarks:** 

Üst blokların özellikleri aşağıdaki şekilde birleştirilir: kenar boşlukları toplanır; üst düzey blokların kenarlıkları atılır ve yalnızca en iç düzeydeki kenarlıklar korunur. Sonuç olarak, bu mod belirtildiğinde, orijinal belgedeki bazı blok biçimlendirmeleri kaybolur.

Öte yandan, tüm birleştirilmiş blok düzeyindeki özellikler belge düğümlerinde depolandığı için, ortaya çıkan belgedeki tüm biçimlendirme değiştirilebilir olacaktır.

### PRESERVE {#PRESERVE}
```
public static int PRESERVE
```


Üst blokların özellikleri özel bir mantıksal yapıya aktarılır ve belge düğümlerinden ayrı olarak depolanır.

 **Remarks:** 

Yalnızca 'body', 'div' ve 'blockquote' HTML öğelerinin kenar boşlukları ve kenarlıkları içe aktarılır. Her HTML öğesinin özellikleri ayrı ayrı depolanır.

Bu mod, HTML belgesinde görülen kenarlıkların ve kenar boşluklarının daha iyi korunmasını ve daha iyi dönüşüm sonuçları elde edilmesini sağlar. Dezavantajı ise, mantıksal yapıda depolanan kenarlık ve kenar boşlukları düzenleme için mevcut olmadığından, ortaya çıkan belgenin değiştirilmesinin zorlaşmasıdır.

Bu mod, blok özelliklerinin içe aktarılmasıyla ilgili MS Word davranışını taklit eder.

### length {#length}
```
public static int length
```


### fromName(String blockImportModeName) {#fromName-java.lang.String}
```
public static int fromName(String blockImportModeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| blockImportModeName | java.lang.String |  |

**Returns:**
int
### getName(int blockImportMode) {#getName-int}
```
public static String getName(int blockImportMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| blockImportMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int blockImportMode) {#toString-int}
```
public static String toString(int blockImportMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| blockImportMode | int |  |

**Returns:**
java.lang.String
