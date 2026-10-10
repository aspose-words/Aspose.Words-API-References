---
title: "HtmlInsertOptions"
linktitle: "HtmlInsertOptions"
second_title: "Aspose.Words Java için"
description: "Java'da MAspose.Words.DocumentBuilder.InsertHtmlSystem.StringAspose.Words.HtmlInsertOptions yöntemine ilişkin seçenekleri belirtir."
type: docs
weight: 381
url: /tr/java/com.aspose.words/htmlinsertoptions/
---

**Inheritance:**
java.lang.Object
```
public class HtmlInsertOptions
```

**M:Aspose.Words.DocumentBuilder.InsertHtml(System.String,Aspose.Words.HtmlInsertOptions)** yöntemine ilişkin seçenekleri belirtir.

 **Examples:** 

Kenarlıkları ve görülen kenar boşluklarını daha iyi korumayı nasıl sağlayacağını gösterir.

```

 final String HTML = "\n                \n                    \n                    \n                        paragraph 1\n                        paragraph 2\n                    \n                    \n                ";

 // Set the new mode of import HTML block-level elements.
 int insertOptions = HtmlInsertOptions.PRESERVE_BLOCKS;

 DocumentBuilder builder = new DocumentBuilder();
 builder.insertHtml(HTML, insertOptions);
 builder.getDocument().save(getArtifactsDir() + "DocumentBuilder.PreserveBlocks.docx");
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [NONE](#NONE) | HTML eklerken varsayılan seçenekleri kullan. |
| [PRESERVE_BLOCKS](#PRESERVE-BLOCKS) | Blok düzeyindeki öğelerin özelliklerini koru. |
| [REMOVE_LAST_EMPTY_PARAGRAPH](#REMOVE-LAST-EMPTY-PARAGRAPH) | Blok düzeyinde bir öğe ile biten HTML'den sonra normal olarak eklenen boş paragrafı kaldır. |
| [USE_BUILDER_FORMATTING](#USE-BUILDER-FORMATTING) | HTML'den eklenen metin için temel biçimlendirme olarak [DocumentBuilder](../../com.aspose.words/documentbuilder/) içinde belirtilen yazı tipi ve paragraf biçimlendirmesini kullan. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String htmlInsertOptionsName)](#fromName-java.lang.String) |  |
| [fromNames(Set htmlInsertOptionsNames)](#fromNames-java.util.Set) |  |
| [getName(int htmlInsertOptions)](#getName-int) |  |
| [getNames(int htmlInsertOptions)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int htmlInsertOptions)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### NONE {#NONE}
```
public static int NONE
```


HTML eklerken varsayılan seçenekleri kullan.

### PRESERVE_BLOCKS {#PRESERVE-BLOCKS}
```
public static int PRESERVE_BLOCKS
```


Blok düzeyindeki öğelerin özelliklerini koru.

 **Remarks:** 

Varsayılan olarak, üst blokların özellikleri birleştirilir ve alt öğelerinde (ör. paragraflar veya tablolar) depolanır. Bu seçenek belirtilirse, her bloğun özellikleri özel bir mantıksal yapıda ayrı ayrı saklanır. Sonuç olarak, bu seçenek HTML belgesindeki bireysel kenarlık ve kenar boşluklarını daha iyi korumayı ve daha iyi dönüşüm sonuçları elde etmeyi sağlar. Dezavantajı, mantıksal yapıda saklanan kenarlık ve kenar boşlukları düzenleme için mevcut olmadığından, ortaya çıkan belgenin değiştirilmesinin zorlaşmasıdır.

Yalnızca 'body', 'div' ve 'blockquote' HTML öğelerinin kenar boşlukları ve kenarlıkları korunur. Her HTML öğesinin özellikleri ayrı ayrı saklanır.

Bu seçenek belirtilirse, Aspose.Words blok özelliklerinin içe aktarımıyla ilgili olarak MS Word davranışını taklit eder.

### REMOVE_LAST_EMPTY_PARAGRAPH {#REMOVE-LAST-EMPTY-PARAGRAPH}
```
public static int REMOVE_LAST_EMPTY_PARAGRAPH
```


Blok düzeyinde bir öğe ile biten HTML'den sonra normal olarak eklenen boş paragrafı kaldır.

 **Remarks:** 

Varsayılan olarak, [DocumentBuilder](../../com.aspose.words/documentbuilder/) HTML'den içe aktarılan son blok düzeyindeki öğenin içe aktarımdan sonra kapatıldığından emin olur ve öğenin ardından bir paragraf sonu ekler. Bu paragraf sonu, HTML'den içe aktarılan içeriği şablon belgenin içeriğinden ayırır. Ancak, bir HTML parçacığı boş bir paragraf içine eklendiğinde, bu paragraf sonu ekstra bir boş paragraf oluşturur. Bu davranış istenmiyorsa, bu seçeneği belirtin.

### USE_BUILDER_FORMATTING {#USE-BUILDER-FORMATTING}
```
public static int USE_BUILDER_FORMATTING
```


HTML'den eklenen metin için temel biçimlendirme olarak [DocumentBuilder](../../com.aspose.words/documentbuilder/) içinde belirtilen yazı tipi ve paragraf biçimlendirmesini kullan.

 **Remarks:** 

Bu seçenek belirtilmezse, [DocumentBuilder](../../com.aspose.words/documentbuilder/) biçimlendirmesi yok sayılır ve metin varsayılan HTML biçimlendirmesiyle eklenir. Sonuç olarak, metin tarayıcılarda görüntülendiği gibi görünür.

Bu seçenek belirtilirse, eklenen metnin biçimlendirmesi [DocumentBuilder](../../com.aspose.words/documentbuilder/) içinde belirtilen biçimlendirmeye dayanır ve metin sanki [DocumentBuilder.write(java.lang.String)](../../com.aspose.words/documentbuilder/\#write-java.lang.String) kullanılarak eklenmiş gibi görünür.

### length {#length}
```
public static int length
```


### fromName(String htmlInsertOptionsName) {#fromName-java.lang.String}
```
public static int fromName(String htmlInsertOptionsName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| htmlInsertOptionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set htmlInsertOptionsNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set htmlInsertOptionsNames)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| htmlInsertOptionsNames | java.util.Set |  |

**Returns:**
int
### getName(int htmlInsertOptions) {#getName-int}
```
public static String getName(int htmlInsertOptions)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| htmlInsertOptions | int |  |

**Returns:**
java.lang.String
### getNames(int htmlInsertOptions) {#getNames-int}
```
public static Set getNames(int htmlInsertOptions)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| htmlInsertOptions | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int htmlInsertOptions) {#toString-int}
```
public static String toString(int htmlInsertOptions)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| htmlInsertOptions | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
