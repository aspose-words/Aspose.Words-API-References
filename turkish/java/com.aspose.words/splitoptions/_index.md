---
title: "SplitOptions"
linktitle: "SplitOptions"
second_title: "Aspose.Words Java için"
description: "Java'da belgenin parçalara nasıl bölüneceğine ilişkin seçenekleri belirtir."
type: docs
weight: 630
url: /tr/java/com.aspose.words/splitoptions/
---

**Inheritance:**
java.lang.Object
```
public class SplitOptions
```

Belgenin bölümlere nasıl ayrılacağına dair seçenekleri belirtir.
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getSplitCriteria()](#getSplitCriteria) | Belgenin parçalara bölünmesi için kriterleri belirtir. |
| [getSplitStyle()](#getSplitStyle) | Belge parçalarına bölünürken [SplitCriteria.STYLE](../../com.aspose.words/splitcriteria/\#STYLE) kullanıldığında paragraf stilini belirtir. |
| [setSplitCriteria(int value)](#setSplitCriteria-int) | Belgenin parçalara bölünmesi için kriterleri belirtir. |
| [setSplitStyle(String value)](#setSplitStyle-java.lang.String) | Belge parçalarına bölünürken [SplitCriteria.STYLE](../../com.aspose.words/splitcriteria/\#STYLE) kullanıldığında paragraf stilini belirtir. |
### getSplitCriteria() {#getSplitCriteria}
```
public int getSplitCriteria()
```


Belgenin parçalara bölünmesi için kriterleri belirtir.

 **Examples:** 

Belgeyi sayfalara göre nasıl bölüneceğini gösterir.

```

 String doc = getMyDir() + "Big document.docx";

 SplitOptions options = new SplitOptions();
 options.setSplitCriteria(SplitCriteria.PAGE);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.1.docx", options);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.2.docx", SaveFormat.DOCX, options);
 
```

**Returns:**
int - İlgili  int  değeri. Döndürülen değer, [SplitCriteria](../../com.aspose.words/splitcriteria/) sabitlerinden biridir.
### getSplitStyle() {#getSplitStyle}
```
public String getSplitStyle()
```


Belge parçalarına bölünürken [SplitCriteria.STYLE](../../com.aspose.words/splitcriteria/\#STYLE) kullanıldığında paragraf stilini belirtir.

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### setSplitCriteria(int value) {#setSplitCriteria-int}
```
public void setSplitCriteria(int value)
```


Belgenin parçalara bölünmesi için kriterleri belirtir.

 **Examples:** 

Belgeyi sayfalara göre nasıl bölüneceğini gösterir.

```

 String doc = getMyDir() + "Big document.docx";

 SplitOptions options = new SplitOptions();
 options.setSplitCriteria(SplitCriteria.PAGE);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.1.docx", options);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.2.docx", SaveFormat.DOCX, options);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili  int  değeri. Değer, [SplitCriteria](../../com.aspose.words/splitcriteria/) sabitlerinden biri olmalıdır. |

### setSplitStyle(String value) {#setSplitStyle-java.lang.String}
```
public void setSplitStyle(String value)
```


Belge parçalarına bölünürken [SplitCriteria.STYLE](../../com.aspose.words/splitcriteria/\#STYLE) kullanıldığında paragraf stilini belirtir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

